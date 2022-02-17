<template>
  <div id="spacer"></div>
  <TextBox text="Country Wellness" />
  <section class="project-details">
    <div>
      <h2 class="">PROJECT BESKRIVELSE</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc nisl enim
        pellentesque sodales id. Donec convallis maecenas viverra venenatis
        tincidunt consectetur pulvinar dignissim. Elit lacus donec at auctor
        commodo, urna auctor quam. Dolor consequat, eget elementum lacinia
        eleifend. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc
        nisl enim pellentesque sodales id. Donec convallis maecenas viverra
        venenatis tincidunt consectetur pulvinar dignissim. Elit lacus donec at
        auctor commodo, urna auctor quam. Dolor consequat, eget elementum
        lacinia eleifend.
      </p>
    </div>
    <div>
      <img
        src="../assets/images/regrow-images/hero-image-regrow.png"
        alt="Regrow hero image"
      />
    </div>
  </section>
  <ProjectDetails
    client="RePot ApS"
    :services="[
      'Rebranding',
      'Logo',
      'Website',
      'Storyscaping - UX',
      'Animations',
      'Animations',
      'Social Media',
    ]"
    :toolsSrc="[
      {
        src: require('../assets/images/skills-icons/file-icons_adobe-photoshop.png'),
      },
      {
        src: require('../assets/images/skills-icons/file-icons_adobe-illustrator.png'),
      },

      {
        src: require('../assets/images/skills-icons/file-icons_adobe-premiere.png'),
      },

      {
        src: require('../assets/images/skills-icons/file-icons_adobe-aftereffects.png'),
      },
      {
        src: require('../assets/images/skills-icons/file-icons_adobe-xd.png'),
      },
      {
        src: require('../assets/images/skills-icons/akar-icons_html-fill.png'),
      },
      {
        src: require('../assets/images/skills-icons/akar-icons_css-fill.png'),
      },
      {
        src: require('../assets/images/skills-icons/brandico_wordpress.png'),
      },
    ]"
    purposeText="Lorem ipsum dolor sit amet, consectetur adipiscing elit.
    Nunc nisl enim pellentesque sodales id. Donec convallis maecenas 
    viverra venenatis tincidunt consectetur pulvinar.
    Donec convallis maecenas viverra venenatis tincidunt
     consectetur pulvinar dignissim."
  />
</template>
<script>
import TextBox from "../components/textBox.vue";
import ProjectDetails from "../components/projectDetails.vue";

export default {
  name: "CountryWellness",
  components: {
    TextBox,
    ProjectDetails,
  },
  mounted() {
    window.scrollTo(0, 0);
  },
};
</script>

<style lang="scss" scoped>
#spacer {
  width: 100%;
  height: 8vh;
}

section.project-details {
  width: 100%;
  & > div:nth-of-type(1) {
    background-color: #f1ebe7;
    padding: 32px;
  }
  & > div:nth-of-type(2) {
    img {
      width: 100%;
    }
  }
  h2 {
    text-transform: uppercase;
    color: #95867d;
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
      background-color: #95867d;
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
@media only screen and (min-width: 1024px) {
  #spacer {
    height: 12vh;
  }
  section.project-details {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 36px;

    & > div:nth-of-type(1) {
      padding: 64px;
    }
    & > div:nth-of-type(2) {
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
    h2 {
      font-size: 158px;
      font-size: 48px;
      padding-bottom: 48px;
      margin-bottom: 48px;

      text-align: left;
      &::after {
        width: 10%;
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
@media only screen and (min-width: 1440px) {
  section.project-details {
    h2 {
      font-size: 158px;
      font-size: 48px;
      padding-bottom: 48px;
      &::after {
        width: 10%;
      }
    }
    p {
      font-size: 22px;
    }
  }
}
</style>
