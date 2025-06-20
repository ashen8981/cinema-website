<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-info">
          <h3>Amadeus IT Group</h3>
          <p>C. Salvador de Madariaga, 1<br>28027 Madrid<br>Spain</p>
        </div>
        <div class="footer-social">
          <p>Follow us on</p>
          <div class="social-links">
            <a href="#" class="social-link">
              <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z" fill="currentColor"/>
              </svg>
            </a>
            <a href="#" class="social-link">
              <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M22.54 6.42a2.78 2.78 0 0 0-1.94-2C18.88 4 12 4 12 4s-6.88 0-8.6.46a2.78 2.78 0 0 0-1.94 2A29 29 0 0 0 1 11.75a29 29 0 0 0 .46 5.33A2.78 2.78 0 0 0 3.4 19c1.72.46 8.6.46 8.6.46s6.88 0 8.6-.46a2.78 2.78 0 0 0 1.94-2 29 29 0 0 0 .46-5.25 29 29 0 0 0-.46-5.33z" fill="currentColor"/>
                <polygon points="9.75,15.02 15.5,11.75 9.75,8.48" fill="#000"/>
              </svg>
            </a>
          </div>
        </div>
      </div>
    </div>
    <!-- Full-width divider -->
    <div class="footer-divider"></div>
    <div class="container">
      <div class="footer-bottom">
        <p>Copyright © 2022 Amadeus Hotels. All rights reserved.</p>
        <p>Photos by <a href="#" class="photo-credit-link">Felix Mooneeram</a> & <a href="#" class="photo-credit-link">Serge Kutuzov</a> on <a href="#" class="photo-credit-link">Unsplash</a></p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
@import '../assets/css/footer.css';
</style>
