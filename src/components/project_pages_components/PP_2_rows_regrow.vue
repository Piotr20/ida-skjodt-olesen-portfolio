<template>
  <section id="2-rows-grid">
    <h2 class="about-me-anim">Brandets budskab</h2>

    <!-- i need multiple headings, you made it weird -->
    <!-- check line 65 in "regrow.vue" -->

    <div class="grid-container">
      <div class="cell-1">
        RePot skal være et brand der har en meget direkte kommunikation, der er seriøs, 
        dramatisk og kraftfuld. Skaberne bag RePot har udtalt at de ikke var blege for at 
        være netop dette. 
        <br><br>
        Brandet er mere en ’bare’ et produkt, de er forgænger for at skabe opmærksomhed 
        omkring bæredygtighed, det er et community, herved blev ReGrow til.
        <br><br>
        ReGrow’s Organizing Idea er ”It is your time”, som illustrere at ’du’ skal tage handling, 
        det er ‘dig’ som har et valg. Brandet er opmærksomhed på at rede planeten, og med dette 
        statement sætter det tiden i fokus, det er nu det skal ske. ReGrow fokusere på den større sag, det handler ikke kun om at sælge et produkt.
      </div>

      <div class="cell-2">

        <!-- fix video - NEEDS STYLING -->
        <video width="500" height="" controls autoplay loop>
        <source src="/src/assets/images/regrow/It is your time_ver1.mp4" type="video/mp4">
        Your browser does not support the video tag.
        </video>
      </div>

      <div class="cell-3">
        <br><br>
        <!-- i need multiple headings -->
        <!-- check line 65 in "regrow.vue" -->
      <h2 class="about-me-anim">Visuelt udtryk</h2>


<!-- this picture is not showing -->
        <img src="../../assets/images/regrow/cards-mockups.png" alt="" />


        3 rem ipsum dolor sit amet consec
      </div>

      
      <div class="cell-4">
        
        <!-- fix image styling on all project pages -->
        <img src="../../assets/images/regrow/styletile_regrow_ver2.png" alt="Styletile Regrow Ver 2" />
        <!-- fix image styling on all project pages -->
      </div>

      <div class="cell-5">
        <br><br> <!-- Needs styling insted of 'breaks' -->
        <!-- i need multiple headings -->
        <!-- check line 65 in "regrow.vue" -->
        <h2 class="about-me-anim">Website</h2>


        <!-- The 3 mockups should be side by side -->
        <!-- fix image styling on all project pages -->
        <img src="../../assets/images/regrow/mockup-frontpage.png" alt="mockup frontpage" />
        <img src="../../assets/images/regrow/mockup-environment.png" alt="mockup environment" />
        <img src="../../assets/images/regrow/mockup-about.png" alt="mockup about us" />
        <!-- fix image styling on all project pages -->


      </div>
      <div class="cell-6">
      </div>
      <div class="cell-7">
      </div>
      <div class="cell-8">
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
  img {
  width: 100%;
} 
/* fix image styling on all project pages */
//tempoary thing i did to style image
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
