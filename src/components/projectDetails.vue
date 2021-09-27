<template>
  <section>
    <div class="client-details">
      <h2>CLIENT</h2>
      <h3>{{ client }}</h3>
    </div>
    <div class="services-details">
      <h2>SERVICES</h2>
      <ul>
        <template v-for="(service, index) in services" :key="index">
          <li>
            <h3>{{ service }}</h3>
          </li>
        </template>
      </ul>
    </div>
    <div class="tools-details">
      <h2>USED TOOLS</h2>
      <div class="grid-container">
        <template v-for="(image, index) in toolsSrc" :key="index">
          <img :src="image" alt="tool icon" />
        </template>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ProjectDetails",
  props: {
    client: String,
    services: Array,
    toolsSrc: Array,
  },
  mounted: function () {
    console.log(this.toolsSrc[0]);
  },
};
</script>

<style lang="scss" scoped>
section {
  width: 100%;
  margin: 24px 0;
  display: grid;

  gap: 24px;
  div {
    padding: 32px;
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
      color: #95867d;
      font-size: 18px;
    }
  }
}
.client-details {
  background-color: #a093f0;
}
.services-details {
  background-color: #e54575;
}
.tools-details {
  background-color: #e877c1;
}
@media only screen and (min-width: 1024px) {
  section {
    margin: 36px 0;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 36px;
    div {
      padding: 64px;
      h2 {
        font-size: 158px;
        font-size: 48px;
        padding-bottom: 48px;
        margin-bottom: 48px;

        text-align: left;
        &::after {
          width: 20%;
          left: 0;
          transform: translateX(0);
        }
      }
      p {
        font-size: 20px;
        text-align: left;
      }
    }
  }
}
</style>
