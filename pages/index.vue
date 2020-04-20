<template>
  <div>
    <p>Welcome.</p>
  </div>
</template>

<script>
export default {
  name: "sample",
  layout: "ore",
  data() {
    return {
      header: {
        title: "Home Page"
      }
    };
  },
  mounted() {
    this.updateHeader();
  },
  methods: {
    updateHeader() {
      this.$nuxt.$emit("updateHeader", this.header.title);
    }
  }
};
</script>

<style lang="scss">
// div{
//   color: red;
// }
</style>