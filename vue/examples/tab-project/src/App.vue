<template>
  <div id="app">
    <Tabs>
      <Tab name="tab1" label="Tab 1">
        <h2>Content for Tab 1</h2>
        <p>This is the content for Tab 1.</p>
      </Tab>
      <Tab name="tab2" label="Tab 2">
        <h2>Content for Tab 2</h2>
        <p>This is the content for Tab 2.</p>
      </Tab>
      <Tab name="tab3" label="Tab 3">
        <h2>Content for Tab 3</h2>
        <p>This is the content for Tab 3.</p>
      </Tab>
    </Tabs>
  </div>
</template>

<script>
import Tab from './components/Tab.vue';

export default {
  name: 'App',
  components: {
    Tabs,
    Tab
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
