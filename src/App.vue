<template>
  <div id="app">
    <Navbar @scroll-to="scrollTo" />
    <Hero />
    <MovieLibrary />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import MovieLibrary from './components/MovieLibrary.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Hero,
    MovieLibrary,
    Contact,
    Footer
  },
  methods: {
    scrollTo(elementId) {
      const element = document.getElementById(elementId)
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' })
      }
    }
  }
}
</script>
