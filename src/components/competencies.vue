<template>
  <section id="competencies">
    <h2 class="competencies-anim">KOMPETENCER OG KVALIFIKATIONER</h2>
    <div class="flex-wrapper">
      <div class="quote-container competencies-anim">
        <span>"</span>
        <h3>
          En effektiv arbejdsdag for mit vedkommende, består af at kunne veksle
          mellem at indgå i grupper og kunne dele erfaringer og ekspertise med
          hinanden, samt at arbejde individuelt og koncentreret omkring en
          opgave. Nye udfordringer tager jeg imod med nysgerrighed og åbenhed.
        </h3>
        <span>"</span>
      </div>

      <ul>
        <li class="competencies-anim">Organisering & planlægning</li>
        <li class="competencies-anim">Pligtopfyldende & pålidelig</li>
        <li class="competencies-anim">Smilende & positiv</li>
        <li class="competencies-anim">Detaljeorienteret</li>
        <li class="competencies-anim">Service minded</li>
        <li class="competencies-anim">Kendskab til kundehåndtering</li>
        <li class="competencies-anim">
          Gode kommunikations egenskaber internationalt
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);
export default {
  name: "Competencies",
  mounted: function () {
    gsap.from(".competencies-anim", {
      scrollTrigger: {
        trigger: "#competencies",
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
  background-color: #a093f0;
  padding: 32px;
  margin: 24px 0;
  h2 {
    text-transform: uppercase;
    color: white;
    font-size: 32px;
    padding-bottom: 32px;
    position: relative;
    text-transform: uppercase;
    &::after {
      content: "";
      position: absolute;
      width: 50%;
      height: 5px;
      background-color: #fff;
      left: 50%;
      bottom: 0;
      transform: translate(-50%, -50%);
    }
  }
}
.flex-wrapper {
  margin-top: 32px;
  display: flex;
  width: 100%;
  flex-direction: column;
}
.quote-container {
  width: 100%;
  padding: 48px 32px;
  background-color: rgba(255, 255, 255, 0.5);
  position: relative;
  h3 {
    color: white;
    font-size: 18px;
  }
  span {
    font-size: 80px;
    color: #a093f0;
    position: absolute;
    transform: translate(-50%, -50%);
    &:nth-of-type(1) {
      left: 25px;
      top: 45px;
    }
    &:nth-of-type(2) {
      right: 0;
      bottom: -85px;
    }
  }
}
ul {
  color: white;
  text-align: left;
  padding: 32px 0;
  font-size: 18px;
  padding-left: 18px;
  li {
    padding: 12px 0;
  }
}

@media only screen and (min-width: 1024px) {
  section {
    width: 100%;
    padding: 64px;
    margin: 36px 0;
    h2 {
      font-size: 158px;
      font-size: 48px;
      padding-bottom: 48px;
      &::after {
        width: 10%;
      }
    }
  }
  .flex-wrapper {
    padding: 64px 0;
    flex-direction: row-reverse;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    margin: 0 auto;
    margin-top: 80px;
  }
  .quote-container {
    width: 45%;
    padding: 100px 64px;
    h3 {
      font-size: 32px;
    }
    span {
      font-size: 144px;
      &:nth-of-type(1) {
        left: 10%;
        top: 15%;
      }
      &:nth-of-type(2) {
        left: 90%;
        top: 93%;
      }
    }
  }
  ul {
    font-size: 24px;
    li {
      padding: 20px 0;
    }
  }
}
@media only screen and (min-width: 1440px) {
  .flex-wrapper {
    width: 90%;
  }
}
</style>
