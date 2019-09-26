<template>
  <div>
    <p>Episodes seen: {{ count }}</p>
    <button @click="count += 1" class="btn-primary">Add 1</button>
    <button @click="count > 0 ? count -= 1 : null" class="btn-danger">Remove 1</button>
  </div>
</template>

<script>
export default {
  props: { episodes_seen: 0 },
  data() {
    return { count: this.episodes_seen };
  }
};
</script>

<style>
</style>

