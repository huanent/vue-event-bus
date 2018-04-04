<template>
    <div>
        <button @click="onClick">ComA点击</button>
    </div>
</template>

<script>
import eventBus from "../event-bus";
export default {
  methods: {
    onClick() {
      eventBus.$emit("ComAClick", "来自ComA的参数");
    }
  }
};
</script>

<style>

</style>
