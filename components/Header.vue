<template>
  <div id="header">
    <h1>{{ title }}</h1>
    <ul>
      <li>
        <nuxt-link to="/">Home Page</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">About</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: ""
    }
  }
};
</script>