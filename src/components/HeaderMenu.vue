<template>
  <div>
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav v-for="titleID in titleIDs" :key="titleID">
        <HeaderLink :titleID="titleID" :key="titleID"/>
      </b-navbar-nav>
    </b-collapse>
  </div>
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
