<template>
  <section id="cv">
    <h2 class="cv-anim">Vil du downloade mit Cv?</h2>
    <a class="cv-anim" href="../assets/CV_Piotr_Pospiech.pdf" download>Download</a>
  </section>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);
export default {
  name: "CvDownload",
  mounted: function () {
    gsap.from(".cv-anim", {
      scrollTrigger: {
        trigger: "#cv",
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
  margin: 24px 0;
  padding: 24px;
  color: #95867d;
  h2 {
    font-size: 26px;
    text-transform: uppercase;
  }
  a {
    text-transform: uppercase;
    background-color: #95867d;
    color: white;
    font-size: 20px;
    padding: 12px 40px;
    display: inline-block;
    margin-top: 24px;
    transition: all 0.3s ease;
    border: 3px solid #95867d;
    cursor: pointer;
    text-decoration: none;
    font-weight: 600;
    &:hover {
      background-color: #fff;
      color: #95867d;
    }
  }
}
@media only screen and (min-width: 1024px) {
  section {
    margin: 36px 0;
    padding: 48px;
    h2 {
      font-size: 32px;
    }
    a {
      font-size: 20px;
      padding: 12px 30px;
      margin-top: 40px;
      align-self: flex-start;
    }
  }
}
</style>
