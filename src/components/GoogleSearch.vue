<template>
  <div>
    <input v-model="searchContent" @keydown.enter="search" />
    <button @click="search">Search</button>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import { googleSearch } from "../core/GoogleSearch";

export default Vue.extend({
  data() {
    return {
      searchContent: "",
    };
  },
  methods: {
    async search() {
      await googleSearch(this.searchContent);
      this.searchContent = "";
    },
  },
});
</script>
