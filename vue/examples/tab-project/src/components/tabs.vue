<template>
  <div class="tabs">
    <div class="tab-header">
      <div
          v-for="(tab, index) in tabs"
          :key="index"
          :class="{ active: activeTab === index }"
          @click="changeTab(index)"
      >
        {{ tab.title }}
      </div>
    </div>
    <div class="tab-content">
      <div v-for="(tab, index) in tabs" :key="index" v-show="activeTab === index">
        {{ tab.content }}
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'BaseTabs',
  setup() {
    const tabs = ref([
      { title: 'Tab 1', content: 'Content for Tab 1' },
      { title: 'Tab 2', content: 'Content for Tab 2' },
      { title: 'Tab 3', content: 'Content for Tab 3' }
    ]);
    const activeTab = ref(0);

    const changeTab = (index) => {
      activeTab.value = index;
    };

    return {
      tabs,
      activeTab,
      changeTab
    };
  }
};
</script>

<style scoped>
.tabs {
  width: 300px;
  margin: 0 auto;
}

.tab-header {
  display: flex;
}

.tab-header div {
  flex: 1;
  padding: 10px;
  text-align: center;
  cursor: pointer;
  background-color: #f0f0f0;
}

.tab-header div.active {
  background-color: #ccc;
}

.tab-content div {
  padding: 20px;
  border: 1px solid #ccc;
}
</style>
