<template>
  <section></section>
</template>

<script>
export default {
  name: "About",
};
</script>

<style lang="scss" scoped>
section {
  width: 100%;
  h2 {
    text-transform: uppercase;
    color: #dfdfdf;
    font-size: 52px;
    padding: 56px 0;
  }
}
@media only screen and (min-width: 1024px) {
  section {
    width: 100%;
    h2 {
      font-size: 158px;
      padding: 100px 0;
    }
  }
}
</style>
