<template>
  <div id="spacer"></div>
  <TextBox text="Smokepins" />
  <section class="project-details">
    <div>
      <h2 class="">PROJEKT BESKRIVELSE</h2>
      <p>
        Smokepins ApS er en dansk startupvirksomhed opstartet af Ole Gravrok i
        2017. Firmaets mission er at konservering af ferskvare skal være nemt og
        tilgængeligt hvor end man befinder sig, heraf deres produkt Smokepins.
        Røgpinde i højkvalitet, håndlavet i Danmark.
        <br /><br />
        Firmaet er kendt for at have medvirket i Løvens Hule i 2019 og igen i
        2020. Det var netop her vi opdagede firmaet og dens potentiale for vores
        eksamensprojekt. Allerede fra første kontakt med Ole, vidste vi at netop
        dette projekt havde en helt særlig mulighed for at imponere.
        <br /><br />
        Formålet med projektet var at skabe en solid brand identitet, som derved
        kunne danne en genkendelighed blandt eksisterende og nye kunder. Samt
        styrke brandet online på tværs af forskellige platforme.
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
    client="Smokepins ApS"
    :services="[
      'Rebranding',
      'Logo',
      'Website',
      'Markedsføring',
      'Sociale medier',
    ]"
    :toolsSrc="[
      {
        src: require('../assets/images/skills-icons/file-icons_adobe-photoshop.png'),
      },
      {
        src: require('../assets/images/skills-icons/file-icons_adobe-illustrator.png'),
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
  name: "Smokepins",
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
