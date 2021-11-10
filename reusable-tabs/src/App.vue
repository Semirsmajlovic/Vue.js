<script setup>
// Vue.js SFC (Single File Component).
// Docs: https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup

import TabsWrapper from "./components/TabsWrapper.vue";
import Tab from "./components/Tab.vue";

</script>

<template>
  <!-- All the <Tab>'s inside the <TabsWrapper> is the default slot. -->
  <TabsWrapper>
    <!-- The content inside the <Tab> such as 'Tab 1' is a slot. -->
    <!-- Slots allows up to write components that can take a variety of content. -->
    <Tab title="Tab 1">Tab 1</Tab>
    <Tab title="Tab 2">Tab 2</Tab>
    <Tab title="Tab 3">Tab 3</Tab>
    <Tab title="Tab 4">Tab 4</Tab>
  </TabsWrapper>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
