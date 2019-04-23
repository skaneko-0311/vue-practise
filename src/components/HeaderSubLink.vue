<template>
  <div>
    <dl>
      <dt></dt>
      <dd v-for="link in this.links" :key="link.id"></dd>
    </dl>
  </div>
</template>

<script>
export default {
  name: "HeaderSubLink",
  props: ["titleID"]
};
</script>