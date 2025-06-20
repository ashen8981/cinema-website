<template>
  <nav class="navbar">
    <div class="nav-container">
      <div class="nav-logo">
        <div class="logo-icon">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M12 2L13.09 8.26L19 7L14.74 12L19 17L13.09 15.74L12 22L10.91 15.74L5 17L9.26 12L5 7L10.91 8.26L12 2Z" fill="#f39c12"/>
          </svg>
        </div>
        <span>Logoipsum</span>
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
