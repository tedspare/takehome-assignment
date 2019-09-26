<template>
  <div class="p-2">
    <h6>{{ name }}</h6>
    <Counter v-bind:episodes_seen="episodes_seen" />
  </div>
</template>

<script>
import Counter from "./Counter.vue";
export default {
  components: { Counter },
  props: {
    id: 0,
    name: "",
    episodes_seen: 0
  }
};
</script>

<style>
</style>
