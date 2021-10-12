<template>
  <div id="app">
    <Header />
    <Hero />
    <main>
      <Intro />
      <Counter />
      <Courses />
      <Events />
      <AboutUs />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Hero from './components/Hero.vue';
import Intro from './components/Intro.vue';
import Counter from './components/Counter.vue';
import Courses from './components/Courses.vue';
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
    Courses,
    Events,
    AboutUs,
    Footer
  }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';

</style>
