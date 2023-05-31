<script>
import Home from './assets/views/Home.vue'
import About from './assets/views/About.vue'
import NotFound from './assets/views/Contact.vue'

const routes = {
  '/': Home,
  '/about': About
}

export default {
  data() {
    return {
      currentPath: window.location.hash
    }
  },
  computed: {
    currentView() {
      return routes[this.currentPath.slice(1) || '/'] || NotFound
    }
  },

}
</script>

<template>
  <a href="#/">Home</a> |
  <a href="#/about">About</a> |
  <a href="#/non-existent-path">Contact</a>
  <component :is="currentView" />
  <div class="aurora" ref="auroraRef"></div>
</template>

<style scoped>
.aurora {
  width: 100%;
  height: 300vh;
  background: linear-gradient(45deg, #1a1a1a, #8a008a, #ff69b4, #ff1493);
  background-size: 200% 200%;
  animation: auroraAnimation 5s ease-in-out infinite;
}

@keyframes auroraAnimation {
  0% {
    background-position: 0% 50%;
  }

  50% {
    background-position: 100% 50%;
  }

  100% {
    background-position: 0% 50%;
  }
}
</style>
