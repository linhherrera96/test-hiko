<template>
  <div class="landing-wrapper">
    <Header></Header>
    <TimeLine></TimeLine>
    <About></About>
    <OurGame></OurGame>
    <Partner></Partner>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "./Header";
import Footer from "./Footer";
import About from "./About";
import Partner from "./Partner";
import OurGame from "./OurGame";
import TimeLine from "./TimeLine";

export default {
  name: "Landing",
  components: {
    Header,
    Footer,
    About,
    Partner,
    OurGame,
    TimeLine,
  },

  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },

  methods: {
    goToTop() {
      window.scrollTo({
        top: 0,
        left: 0,
        behavior: "smooth",
      });
    },

    handleScroll(event) {
      // Any code to be executed when the window is scrolled
      this.isUserScrolling = window.scrollY > 0;
    },
  },
};

import "@/assets/scss/toppage.scss";
</script>
