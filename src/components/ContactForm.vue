<template>
  <form @submit.prevent="submitForm" class="contact-form">
    <div class="form-row">
      <div class="form-group">
        <label for="firstName">First Name *</label>
        <input 
          type="text" 
          id="firstName" 
          v-model="form.firstName"
          required
        >
      </div>
      <div class="form-group">
        <label for="lastName">Last Name *</label>
        <input 
          type="text" 
          id="lastName" 
          v-model="form.lastName"
          required
        >
      </div>
    </div>
    
    <div class="form-group">
      <label for="email">Email *</label>
      <input 
        type="email" 
        id="email" 
        v-model="form.email"
        required
      >
    </div>
    
    <div class="form-group">
      <label for="telephone">Telephone</label>
      <input 
        type="tel" 
        id="telephone" 
        v-model="form.telephone"
      >
    </div>
    
    <div class="form-group">
      <label for="message">Message</label>
      <textarea 
        id="message" 
        v-model="form.message"
        rows="4"
      ></textarea>
    </div>
    
    <p class="required-text">* required fields</p>
    
    <div class="checkbox-group">
      <input 
        type="checkbox" 
        id="terms" 
        v-model="form.agreeToTerms"
        required
      >
      <label for="terms">I agree to the <a href="#" class="terms-link">Terms & Conditions</a></label>
    </div>
    
    <button type="submit" class="submit-btn">SUBMIT</button>
  </form>
</template>

<script>
export default {
  name: 'ContactForm',
  data() {
    return {
      form: {
        firstName: '',
        lastName: '',
        email: '',
        telephone: '',
        message: '',
        agreeToTerms: false
      }
    }
  },
  methods: {
    submitForm() {
      if (this.form.agreeToTerms) {
        alert('Form submitted successfully!')
        this.resetForm()
      } else {
        alert('Please agree to the Terms & Conditions')
      }
    },
    resetForm() {
      this.form = {
        firstName: '',
        lastName: '',
        email: '',
        telephone: '',
        message: '',
        agreeToTerms: false
      }
    }
  }
}
</script>

<style scoped>
@import '../assets/css/contact-form.css';
</style>
