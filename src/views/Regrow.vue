<template>
  <div id="spacer"></div>
  <TextBox text="regrow" />
</template>

<script>
import TextBox from "../components/textBox.vue";
export default {
  components: {
    TextBox,
  },
};
</script>

<style lang="scss" scoped>
#spacer {
  width: 100%;
  height: 8vh;
}
@media only screen and (min-width: 1024px) {
  #spacer {
    height: 12vh;
  }
}
</style>
