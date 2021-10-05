<template>
  <IntroSection />
  <TextBox text="portfolio" />
  <Projects />
  <TextBox text="about" />
  <About />
  <AboutMe />
  <TechSkills />
  <Competencies />
  <Language />
  <TextBox text="cv" />
  <WorkExpierience />
  <Education />
  <FreelanceProjects />
  <CvDownload />
  <Contact />
</template>

<script>
import IntroSection from "../components/introSection.vue";
import TextBox from "../components/textBox.vue";
import Projects from "../components/projectsSection.vue";
import About from "../components/about.vue";
import AboutMe from "../components/aboutMe.vue";
import TechSkills from "../components/technicalSkills.vue";
import Competencies from "../components/competencies.vue";
import Language from "../components/language.vue";
import WorkExpierience from "../components/workExpierience.vue";
import Education from "../components/education.vue";
import FreelanceProjects from "../components/freelanceProjects.vue";
import CvDownload from "../components/cvDownloadSection.vue";
import Contact from "../components/contact.vue";

export default {
  name: "Home",
  mounted() {
    window.scrollTo(0, 0);
  },
  components: {
    IntroSection,
    Projects,
    TextBox,
    About,
    AboutMe,
    TechSkills,
    Competencies,
    Language,
    WorkExpierience,
    Education,
    FreelanceProjects,
    CvDownload,
    Contact,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  scroll-behavior: smooth;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
