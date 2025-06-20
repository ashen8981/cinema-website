<template>
  <section id="contact" class="contact">
    <div class="container">
      <div class="contact-content">
        <div class="contact-form-section">
          <h2>How to reach us</h2>
          <p class="contact-subtitle">Lorem ipsum dolor sit amet, consectetur.</p>
          <ContactForm />
        </div>
        <MapSection />
      </div>
    </div>
  </section>
</template>

<script>
import ContactForm from './ContactForm.vue'
import MapSection from './MapSection.vue'

export default {
  name: 'Contact',
  components: {
    ContactForm,
    MapSection
  }
}
</script>

<style scoped>
@import '../assets/css/contact.css';
</style>
