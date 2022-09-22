<template>
  <div id="app">
    <Header :pages="pages" />
    <Hero />
    <main>
      <Intro />
      <Counter />
      <Courses />
      <Learn />
      <Events />
      <AboutUs />
    </main>
    <Footer :pages="pages" />
  </div>
</template>

<script>
import axios from 'axios';
import Header from './components/Header.vue'
import Hero from './components/Hero.vue';
import Intro from './components/Intro.vue';
import Counter from './components/Counter.vue';
import Courses from './components/Courses.vue';
import Learn from './components/Learn.vue';
import Events from './components/Events.vue';
import AboutUs from './components/AboutUs.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    Intro,
    Counter,
    Learn,
    Courses,
    Events,
    AboutUs,
    Footer
  },
  data() {
    return {
      pages: [
        "Home",
        "Pages",
        "Courses",
        "Features",
        "Blog",
        "Shop"
      ],
    }      
  },
  created() {
    axios.get('https://www.procidaisland.net/api/')
          .then((res) => {
            console.log(res);
          })
  }
}
</script>

<style lang="scss">

@import './assets/style/common.scss';

</style>
