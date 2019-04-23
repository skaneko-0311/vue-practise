<template>
  <header>
    <HeaderLogo/>
    <HeaderMenu/>
  </header>
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
