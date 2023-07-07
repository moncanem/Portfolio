<template>
  <div :class="modeClass">
    <!-- Your application content here -->
    <button @click="toggleMode">Toggle Dark Mode</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      darkMode: false
    };
  },
  methods: {
    toggleMode() {
      this.darkMode = !this.darkMode;
    }
  },
  computed: {
    modeClass() {
      return this.darkMode ? 'dark-mode' : 'light-mode';
    }
  }
};
</script>

<style>
/* Light mode styles */
.light-mode {
  background-color: #ffffff;
  color: #000000;
}

/* Dark mode styles */
.dark-mode {
  background-color: #000000;
  color: #ffffff;
}
</style>