<template>
  <div>
    <ol v-for="titleID in titleIDs" :key="titleID">
        <LinkSolver v-bind:titleID="titleID" />
    </ol>
  </div>
</template>

<script>
import LinkSolver from "./LinkSolver"
export default {
  name: "HeaderMenu",
  components: {
      LinkSolver
  },
  data: function() {
      return {
          titleIDs: [1, 2, 3, 4, 5, 6, 7, 8, 9]
      }
  },
  methods: {
    makeHeaderLinks: function(menu) {
      let out = '<a href="' + menu.link + '">' + menu.title + "</a>";
      return out;
    }
  }
};
</script>

<style scoped>
ol {
  display: inline-block;
}
</style>
