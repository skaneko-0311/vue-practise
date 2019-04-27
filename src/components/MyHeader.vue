<template>
  <b-navbar toggleable="lg" type="dark" variant="info">
    <HeaderLogo/>
    <HeaderMenu/>
  </b-navbar>
</template>

<script>
import HeaderLogo from "./HeaderLogo.vue";
import HeaderMenu from "./HeaderMenu.vue";
export default {
  name: "MyHeader",
  components: {
    HeaderLogo,
    HeaderMenu
  }
};
</script>
