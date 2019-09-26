<template>
  <div>
    <p>Current count: {{ count }}</p>
    <button v-on:click="count += 1" class="btn-primary">Add 1</button>
    <button v-on:click="count -= 1" class="btn-danger">Remove 1</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 69
    };
  }
};
</script>

<style>
</style>

