<template>
  <div class="container">
    <div class="tab" id="tab" @click="animateTab">
      <a href="#projects">Projects</a>
    </div>
    <div class="content">
      <h1>Luca :)</h1>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    animateTab() {
      const tab = document.getElementById('tab');
      tab.classList.add('animated', 'fadeIn');
      setTimeout(() => {
        tab.classList.remove('fadeIn');
      }, 1000);
    },
  },
};
</script>

<style>
body,
h1,
p {
  margin: 0;
  padding: 0;
}

body {
  background-color: #000;
  color: #fff;
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
}

.container {
  position: relative;
  padding: 45px;
}

.content {
  text-align: center;
  position: relative;
  z-index: 1;
}

h1 {
  font-size: 4rem;
}

.tab {
  position: absolute;
  top: 30px; /* Adjust the positioning as needed */
  left: 50%;
  transform: translateX(-50%);
  z-index: 2;
}

.tab a {
  text-decoration: none;
  color: #fff;
  font-size: 18px; /* Adjust the font size as needed */
  background-color: transparent;
  border: none;
  padding: 0;
  transition: color 0.3s;
}

.tab a:hover {
  color: #888;
}

/* Add animation classes */

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.animated {
  animation-fill-mode: both;
}

.fadeIn {
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-delay: 0.5s;
}
</style>
