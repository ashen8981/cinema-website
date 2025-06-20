<template>
  <div class="search-container">
    <div class="search-icon">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="11" cy="11" r="8" stroke="#999" stroke-width="2"/>
        <path d="m21 21-4.35-4.35" stroke="#999" stroke-width="2"/>
      </svg>
    </div>
    <input 
      type="text" 
      placeholder="Search title and add to grid"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
      class="search-input"
    >
  </div>
</template>

<script>
export default {
  name: 'SearchBar',
  props: {
    modelValue: {
      type: String,
      default: ''
    }
  },
  emits: ['update:modelValue']
}
</script>

<style scoped>
@import '../assets/css/search-bar.css';
</style>
