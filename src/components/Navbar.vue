<template>
  <nav class="navbar">
    <div class="nav-container">
      <div class="nav-logo">
        <div class="logo-icon">
          <img src="@/assets/icons/logo.svg" alt="Logo" class="logo-img" />
        </div>
      </div>
      <ul class="nav-menu" :class="{ active: isMenuOpen }">
        <li>
          <a 
            href="#home" 
            @click="handleNavClick('home')"
            :class="{ active: activeSection === 'home' }"
          >
            HOME
          </a>
        </li>
        <li>
          <a 
            href="#screens" 
            @click="handleNavClick('screens')"
            :class="{ active: activeSection === 'screens' }"
          >
            OUR SCREENS
          </a>
        </li>
        <li>
          <a 
            href="#schedule" 
            @click="handleNavClick('schedule')"
            :class="{ active: activeSection === 'schedule' }"
          >
            SCHEDULE
          </a>
        </li>
        <li>
          <a 
            href="#library" 
            @click="handleNavClick('library')"
            :class="{ active: activeSection === 'library' }"
          >
            MOVIE LIBRARY
          </a>
        </li>
        <li>
          <a 
            href="#contact" 
            @click="handleNavClick('contact')"
            :class="{ active: activeSection === 'contact' }"
          >
            LOCATION & CONTACT
          </a>
        </li>
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
      isMenuOpen: false,
      activeSection: 'home'
    }
  },
  mounted() {
    // Set initial active section and add scroll listener
    this.updateActiveSection()
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen
    },
    handleNavClick(elementId) {
      this.activeSection = elementId
      this.$emit('scroll-to', elementId)
      this.isMenuOpen = false
    },
    handleScroll() {
      // Throttle scroll events for performance
      if (!this.scrollTimeout) {
        this.scrollTimeout = setTimeout(() => {
          this.updateActiveSection()
          this.scrollTimeout = null
        }, 100)
      }
    },
    updateActiveSection() {
      const sections = ['home', 'screens', 'schedule', 'library', 'contact']
      const scrollPosition = window.scrollY + 100 // Offset for navbar height
      
      for (let i = sections.length - 1; i >= 0; i--) {
        const section = document.getElementById(sections[i])
        if (section && section.offsetTop <= scrollPosition) {
          this.activeSection = sections[i]
          break
        }
      }
    }
  }
}
</script>

<style scoped>
@import '../assets/css/navbar.css';
</style>
