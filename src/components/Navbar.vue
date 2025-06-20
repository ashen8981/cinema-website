<template>
  <nav class="navbar">
    <div class="nav-container">
      <div class="nav-logo">
        <div class="logo-icon">
          <img src="@/assets/icons/logo.svg" alt="Logo" class="logo-img" />
        </div>
  
      </div>
      <ul class="nav-menu" :class="{ active: isMenuOpen }">
        <li><a href="#home" @click="handleNavClick('home')">HOME</a></li>
        <li><a href="#screens" @click="handleNavClick('screens')">OUR SCREENS</a></li>
        <li><a href="#schedule" @click="handleNavClick('schedule')">SCHEDULE</a></li>
        <li><a href="#library" @click="handleNavClick('library')">MOVIE LIBRARY</a></li>
        <li><a href="#contact" @click="handleNavClick('contact')">LOCATION & CONTACT</a></li>
      </ul>
      <div class="hamburger" :class="{ active: isMenuOpen }" @click="toggleMenu">
        <div class="hamburger-line"></div>
        <div class="hamburger-line"></div>
        <div class="hamburger-line"></div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      isMenuOpen: false
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen
    },
    handleNavClick(elementId) {
      this.$emit('scroll-to', elementId)
      this.isMenuOpen = false
    }
  }
}
</script>

<style scoped>
@import '../assets/css/navbar.css';
</style>
