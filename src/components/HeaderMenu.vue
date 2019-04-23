<template>
  <nav>
    <template v-for="titleID in titleIDs">
      <HeaderLink :titleID="titleID" :key="titleID" class="header-link"/>
    </template>
  </nav>
</template>

<script>
import HeaderLink from "./HeaderLink.vue";
export default {
  name: "HeaderMenu",
  components: {
    HeaderLink
  },
  data: function() {
    return {
      titleIDs: [1, 2, 3, 4, 5, 6, 7, 8, 9]
    };
  }
};
</script>
<style scoped>
.header-link {
  display: inline;
}
</style>
