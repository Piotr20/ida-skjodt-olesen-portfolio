<template>
  <section id="language">
    <h2 class="language-anim">SPROG</h2>
    <p class="language-anim">
      Gennem min internationale uddannelse på Erhvervs Akademiet Aarhus, har jeg udviklede mine sproglige egenskaber, 
      samt udvidet min kulturelle forståelse.
    </p>
    <div class="flags-container">
      <div class="language-anim">
        <img
          src="..\assets\images\emojione_flag-for-denmark.png"
          alt="Danish flag"
        />
        <div><span>DANSK</span><br /><span>
          <ul>
            <li>Forståelse: Flydende/modersmål</li>
            <li>Tale: Flydende/modersmål</li>
            <li>Læse: Flydende/modersmål</li>
            <li>Skrive: Flydende/modersmål</li>
          </ul>
</span></div>
      </div>
      <div class="language-anim">
        <img
          src="..\assets\images\emojione_flag-for-united-kingdom.png"
          alt="British flag"
        />

        <div>
          <span>ENGELSK</span> <br /><span>
            <ul>
              <li>Forståelse: Flydende/modersmål</li>
              <li>Tale: Flydende/modersmål</li>
              <li>Læse: Flydende/modersmål</li>
              <li>Skrive: Flydende/modersmål</li>
            </ul> 
</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);
export default {
  name: "Language",
  mounted: function () {
    gsap.from(".language-anim", {
      scrollTrigger: {
        trigger: "#language",
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
  background-color: #e54575;
  padding: 32px;
  margin: 24px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  h2 {
    text-transform: uppercase;
    color: white;
    font-size: 32px;
    padding-bottom: 32px;
    margin-bottom: 32px;
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
  p {
    color: white;
    font-size: 18px;
    width: 100%;
  }
}
.flags-container {
  padding-top: 64px;
  display: flex;
  flex-direction: column;
  & > div {
    width: fit-content;
    display: flex;
    align-items: center;
    margin-bottom: 16px;
    img {
      width: 50px;
    }
  }
  div {
    color: white;
    font-size: 18px;
    text-align: left;
    padding-left: 32px;
    span {
      font-weight: 600;
    }
    span:nth-of-type(2) {
      font-weight: 300;
      font-size: 14px;
    }
  }
}

@media only screen and (min-width: 1024px) {
  section {
    width: 100%;
    padding: 64px;
    margin: 36px 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    h2 {
      font-size: 158px;
      font-size: 48px;
      padding-bottom: 48px;
    }
    p {
      font-size: 22px;
      width: 75ch;
    }
  }
  .flags-container {
    padding-top: 80px;
    div {
      margin: 12px 0;
      font-size: 20px;
      align-items: flex-start;
      display: flex;
      justify-content: center;
      img {
        width: 70px;
      }
      br {
        display: none;
      }
      div {
        display: flex;
        flex-direction: column;

        span:nth-of-type(2) {
          margin-top: 6px;
          font-size: 16px;
        }
      }
    }
    h3 {
      font-size: 20px;
    }
  }
}
@media only screen and (min-width: 1440px) {
  section p {
    font-size: 22px;
  }
  .flags-container h3 {
    font-size: 22px;
  }
}
</style>
