<template>
  <div class="pane" v-show="sw">
    <slot></slot>
  </div>
</template>
<script>
export default {
  name: "pane", //为getTabs()遍历所有name为pane的子组件做准备，所以这里起个name
  data: function() {
    return { sw: true };
  },
  props: {
    name: {
      //pane的标识
      type: String
    },
    label: {
      //标签页标题
      type: String,
      default: "as"
    }
  },
  methods: {
    updateNav() {
      this.$parent.updateNav();
    }
  },
  watch: {
    label() {
      this.updateNav();
    }
  },
  mounted() {
    this.updateNav();
  }
};
</script>