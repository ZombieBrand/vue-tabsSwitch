<template>
  <div id="app">
    <tabs v-model="activeKey">
      <pane label="标签一" name="a">
        <p>标签一的内容</p>
        <p>标签一的内容</p>
        <p>标签一的内容</p>
      </pane>
      <pane label="标签二" name="b">标签二的内容</pane>
      <pane label="标签三" name="c">标签三的内容</pane>
    </tabs>
    <tabs v-model="activeKey1">
      <pane label="标签一" name="1">标签1的内容</pane>
      <pane label="标签二" name="2">标签2的内容</pane>
      <pane label="标签三" name="3">标签3的内容</pane>
    </tabs>
  </div>
</template>

<script>
import tabs from "./components/tabs";
import pane from "./components/pane";

export default {
  name: "App",
  components: {
    tabs,
    pane
  }
};
</script>
