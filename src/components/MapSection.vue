<template>
  <div class="map-section">
    <div class="map-container">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3037.4849853609544!2d-3.6919!3d40.4168!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0xd42287c8b3d3b7b%3A0x8b8b8b8b8b8b8b8b!2sMadrid%2C%20Spain!5e0!3m2!1sen!2sus!4v1635000000000!5m2!1sen!2sus"
        width="100%"
        height="400"
        style="border:0;"
        allowfullscreen=""
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade">
      </iframe>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MapSection'
}
</script>

<style scoped>
@import '../assets/css/map-section.css';
</style>
