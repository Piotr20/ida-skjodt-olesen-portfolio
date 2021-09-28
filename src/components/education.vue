<template>
  <section id="education">
    <div class="grid-conainer">
      <div class="side-box-container">
        <SideHeading title="Education" />
      </div>
      <div class="education-box education-anim">
        <h2>Erhvervsgymnasiet Grindsted</h2>
        <h3>2015 - 2018</h3>
        <span>Højere Teknisk Eksamen (HTX) - Kommunikation & IT</span>
      </div>
      <div class="education-box education-anim">
        <h2>Business Academy Aarhus</h2>
        <h3>2019 - 2021</h3>
        <span>Multimedia Design AP - Content Creation</span>
      </div>
    </div>
  </section>
</template>

<script>
import SideHeading from "../components/sideHeadingBox.vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);
export default {
  name: "Education",
  components: {
    SideHeading,
  },
  mounted: function () {
    gsap.from(".education-anim", {
      scrollTrigger: {
        trigger: "#education",
        start: "top 70%",
      },
      opacity: 0,
      y: 30,
      duration: 0.3,
      stagger: 0.3,
      ease: "power1.inOut",
    });
  },
};
</script>

<style lang="scss" scoped>
section {
  width: 100%;
}
.grid-conainer {
  display: grid;
  width: 100%;
  grid-auto-rows: minmax(min-content, max-content);
  grid-gap: 24px;
}
.education-box {
  background-color: #e877c1;
  padding: 24px;
  text-align: left;
  color: white;
  h2 {
    font-size: 26px;
    text-transform: uppercase;
  }
  h3 {
    font-size: 20px;
    padding-top: 8px;
    margin-bottom: 24px;
  }
  span {
    font-size: 18px;
  }
  ul {
    margin-top: 8px;
    padding-left: 16px;
    li {
      padding: 8px 0;
    }
  }
}
@media only screen and (min-width: 1024px) {
  .grid-conainer {
    grid-template-columns: 1fr 1fr;
    grid-auto-rows: minmax(min-content, max-content);
    grid-gap: 36px;
    h2 {
      font-size: 40px;
    }
    h3 {
      font-size: 32px;
      padding-top: 8px;
      margin-bottom: 24px;
    }
    span {
      font-size: 24px;
    }
    ul {
      margin-top: 8px;
      font-size: 20px;

      padding-left: 24px;
      li {
        padding: 8px 0;
      }
    }
  }
  .side-box-container {
    grid-row: 1/3;
    grid-column: 2/3;
  }
}
</style>
