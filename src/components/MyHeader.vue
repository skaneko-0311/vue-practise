<template>
  <div>
    <a href>
      <img src="../assets/company_logo.png">
    </a>
    <HeaderMenu />
  </div>
</template>

<script>
import HeaderMenu from "./HeaderMenu.vue";
export default {
  name: "MyHeader",
  components: {
    HeaderMenu,
  }
};
</script>

<style scoped>
img:hover {
  opacity: 0.5;
  -webkit-transition: 0s;
  transition: 0s;
}
</style>
