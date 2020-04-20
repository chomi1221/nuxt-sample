<template>
  <div>
    <p>This is my profile.</p>
  </div>
</template>

<script>
export default {
  name: "sample",
  layout: "ore",
  data() {
    return {
      header: {
        title: "About"
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