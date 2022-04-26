<template>
  <section id="2-rows-grid">
    <h2 class="about-me-anim">{{ headingText }}</h2>
    <div class="grid-container">
      <div class="cell-1">
        Herved blev ReGrow til, et brand der har en meget direkte kommunikation, der er seriøs, dramatisk og
        kraftfuld. Skaberne bag RePot har udtalt at de ikke var blege for at være netop dette. ReGrow’s
        Organizing Idea er ”It is your time”, som illustrere at ’du’ skal tage handling, det er ‘dig’ som har
        et valg.
        <br />
        Brandet er opmærksomhed på at rede planeten, og med dette statement sætter det tiden i fokus, det er
        nu det skal ske. ReGrow fokusere på den større sag, det handler ikke kun om at sælge et produkt.
      </div>
      <div class="cell-2">
        <!-- NEEDS STYLING -->
        <!-- <img src="../../assets/images/regrow/business_card_mockup_bag.png" alt="" /> -->
        <!-- fix image styling on all project pages -->
      </div>
      <div class="cell-3">3 rem ipsum dolor sit amet consec</div>
      <div class="cell-4">
        <img src="../../assets/images/logo.png" alt="" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "TwoRowsLayout_smokepins",
  props: {
    headingText: String,
  },
};
</script>

<style lang="scss" scoped>
section {
  background-color: #f1ebe7;
  padding: 32px;
}
h2 {
  color: #95867d;
  text-transform: uppercase;
  font-size: 32px;
  padding-bottom: 32px;
  position: relative;

  &::after {
    content: "";
    position: absolute;
    width: 50%;
    height: 5px;
    background-color: #95867d;
    left: 50%;
    bottom: 0;
    transform: translate(-50%, -50%);
  }
}
.grid-container {
  padding: 24px 0;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  grid-gap: 24px;
  div {
    text-align: left;
    &:nth-of-type(2) {
      display: flex;
      justify-content: center;
      align-items: center;
    }
    &:nth-of-type(4) {
      display: flex;
      justify-content: center;
      align-items: center;
    } //the type is reffering to which grid box
  }
}
@media only screen and (min-width: 1024px) {
  section {
    padding: 64px;
  }
  .grid-container {
    padding: 48px 0;
  }
  h2 {
    text-align: left;
    font-size: 32px;
    padding-bottom: 14px;
    &::after {
      transform: translateX(0);
      left: 0;
      width: 4%;
    }
  }
}
</style>
