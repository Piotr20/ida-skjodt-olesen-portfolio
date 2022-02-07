<template>
  <Header />
  <router-view />
</template>

<script>
import Header from "../src/components/header.vue";
export default {
  components: {
    Header,
  },
};
</script>

<style lang="scss">
#app {
  text-align: center;
  color: #2c3e50;
  h1,
  h2,
  h3,
  h4,
  h5,
  h6,
  a {
    font-family: "DM Sans", sans-serif;
  }
  span,
  p,
  div {
    font-family: "Lato", sans-serif;
  }
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
