<template>
  <section id="home">
    <h1 class="intro-anim">Halløj!</h1>
    <h2 class="intro-anim">
      Jeg er <strong>digital designer</strong> med interesse i
      <strong>motion graphic design</strong>
    </h2>
  </section>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

export default {
  data() {
    return {};
  },
  name: "IntroSection",
  props: {},
  mounted: function () {
    console.log("I work");
    gsap.from(".intro-anim", {
      scrollTrigger: "#home", // start the animation when ".box" enters the viewport (once)
      opacity: 0,
      y: 30,
      duration: 0.3,
      stagger: 0.3,
      ease: "power1.inOut",
    });
  },
};
</script>

<style scoped lang="scss">
section {
  width: 100%;
  height: 100vh;
  background-color: #b6abf9;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-end;
  & > * {
    color: white;
  }
  h1 {
    font-size: 192px;
    border-bottom: 10px solid white;
  }
  h2 {
    margin-top: 14vh;
    margin-bottom: 12vh;
    font-weight: normal;
    padding-left: 10px;
    padding-right: 10px;
  }
}

@media only screen and (min-width: 1024px) {
  section {
    h1 {
      font-size: 288px;
      border-bottom: 10px solid white;
    }
    h2 {
      font-size: 24px;
      margin-top: 18vh;
      margin-bottom: 10vh;
    }
  }
}
</style>
