<template>
  <section id="work-expierience">
    <div class="grid-conainer">
      <div class="side-box-container">
        <SideHeading title="Work experience" />
      </div>
      <div class="work-expierience-box work-expierience-anim">
        <h2>MENY SØNDER OMME</h2>
        <h3>Juni 2014 - Nuværende</h3>
        <span>Service medarbejder</span>
      </div>
      <div class="work-expierience-box work-expierience-anim">
        <h2>BILLUND AIRPORT</h2>
        <h3>Maj 2019 - September 2021</h3>
        <span>Kasseassistent i Sales</span>
      </div>
      <div class="work-expierience-box work-expierience-anim">
        <h2>VIRAL FILM (INTERNSHIP)</h2>
        <h3>Januar 2021 - April 2021</h3>
        <span>Motion Graphics praktikant</span>
        <ul>
          <li>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc nisl
            enim pellentesque sodales id.
          </li>
          <li>
            Donec convallis maecenas viverra venenatis tincidunt consectetur
            pulvinar dignissim. Elit lacus donec at auctor commodo, urna auctor
            quam.
          </li>
          <li>Dolor consequat, eget elementum lacinia eleifend.</li>
        </ul>
      </div>
      <div class="work-expierience-box work-expierience-anim">
        <h2>VIRAL FILM (FulLTIME)</h2>
        <h3>August 2021 - September 2021</h3>
        <span>Digital Designer og Animator</span>
        <ul>
          <li>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc nisl
            enim pellentesque sodales id.
          </li>
          <li>
            Donec convallis maecenas viverra venenatis tincidunt consectetur
            pulvinar dignissim. Elit lacus donec at auctor commodo, urna auctor
            quam.
          </li>
          <li>Dolor consequat, eget elementum lacinia eleifend.</li>
        </ul>
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
  name: "WorkExpierience",
  components: {
    SideHeading,
  },
  mounted: function () {
    gsap.from(".work-expierience-anim", {
      scrollTrigger: {
        trigger: "#work-expierience",
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
}
.grid-conainer {
  display: grid;
  width: 100%;
  grid-auto-rows: minmax(min-content, max-content);
  grid-gap: 24px;
}
.work-expierience-box {
  background-color: #a093f0;
  padding: 24px;
  text-align: left;
  color: white;
  h2 {
    font-size: 26px;
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
  section {
    margin: 36px 0;
  }
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
    grid-row: 1/5;
  }
}
</style>
