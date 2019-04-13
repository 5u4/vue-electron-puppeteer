<template>
  <div>
    <google-search></google-search>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import GoogleSearch from "./components/GoogleSearch.vue";

export default Vue.extend({
  components: {
    GoogleSearch,
  },
});
</script>
