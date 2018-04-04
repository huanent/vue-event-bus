<template>
    <div>{{msg}}</div>
</template>

<script>
import eventBus from "../event-bus";
export default {
  data() {
    return {
      msg: "等待事件触发"
    };
  },
  mounted() {
    eventBus.$on("ComAClick", p => {
      this.msg = "已经监听到ComAClick事件:" + p;
    });
  }
};
</script>

<style>

</style>
