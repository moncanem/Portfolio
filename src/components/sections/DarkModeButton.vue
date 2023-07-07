<template>
  <button class="dark-mode-button" @click="toggleDarkMode">
    {{ darkMode ? 'Light Mode' : 'Dark Mode' }}
  </button>
</template>

<script>
export default {
  data() {
    return {
      darkMode: false,
    };
  },
  methods: {
    toggleDarkMode() {
      this.darkMode = !this.darkMode;
      document.body.classList.toggle('dark-mode');
        this.$emit('dark-mode-toggle', !this.darkMode);
    },
  },
};
</script>

<style>
.dark-mode-button {
  position: fixed;
  bottom: 20px;
  right: 20px;
  padding: 10px 20px;
  background-color: #333;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  z-index: 1;
}

.dark-mode-button:hover {
  background-color: #555;
}

.dark-mode {
  background-color: #222;
  color: #fff;
}
</style>
