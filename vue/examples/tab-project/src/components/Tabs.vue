<template>
  <div class="tabs">
    <div class="tabs-nav">
      <button
          v-for="tab in tabs"
          :key="tab.name"
          :class="{ active: tab.name === activeTab }"
          @click="selectTab(tab.name)"
      >
        {{ tab.label }}
      </button>
    </div>
    <div class="tabs-content">
      <slot :activeTab="activeTab"></slot>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeTab: null,
      tabs: []
    };
  },
  methods: {
    selectTab(tabName) {
      this.activeTab = tabName;
    },
    addTab(tab) {
      if (this.tabs.length === 0) {
        this.activeTab = tab.name;
      }
      this.tabs.push(tab);
    }
  }
};
</script>

<style scoped>
.tabs-nav {
  display: flex;
  border-bottom: 1px solid #ccc;
}
.tabs-nav button {
  padding: 10px 20px;
  cursor: pointer;
}
.tabs-nav button.active {
  border-bottom: 2px solid #42b983;
  color: #42b983;
}
.tabs-content {
  padding: 20px;
  border: 1px solid #ccc;
}
</style>
