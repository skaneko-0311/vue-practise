<template>
  <div>
    <a href>
      <!-- Why can I not show the image ? ;( -->
      <img :src="src">
    </a>
  </div>
</template>

<script>
export default {
  name: "HeaderLogo",
  data: function() {
    return {
      src: "../assets/company_logo.png"
    };
  }
};
</script>