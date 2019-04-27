<template>
  <div>
    <b-navbar-brand href="#">
      <img :src="image_src">
    </b-navbar-brand>
  </div>
</template>

<script>
export default {
  name: "HeaderLogo",
  data: function() {
    return {
      image_src: require("../assets/company_logo.png")
    };
  }
};
</script>