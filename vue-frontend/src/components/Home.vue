<template>
  <div>
    <Instructions v-bind:complete="true" />
    <Show
      v-for="show in shows"
      :key="show.id"
      :id="show.id"
      :name="show.name"
      :episodes_seen="show.episodes_seen"
    />
    <div class="p-2">
      <input type="text" v-model="show_name" placeholder="Show Name" />
      <button @click="addShow" class="btn-primary">Add Show</button>
    </div>
  </div>
</template>

<script>
import Instructions from "./Instructions.vue";
import Show from "./Show.vue";

export default {
  components: {
    Instructions,
    Show
  },
  data() {
    return {
      shows: [
        { id: 1, name: "Game of Thrones", episodes_seen: 0 },
        { id: 2, name: "Naruto", episodes_seen: 220 },
        { id: 3, name: "Black Mirror", episodes_seen: 3 }
      ],
      show_name: ""
    };
  },
  methods: {
    addShow() {
      return this.shows.push({
        id: this.shows.length + 1,
        name: this.show_name,
        episodes_seen: 0
      });
    }
  }
};
</script>

<style>
</style>


