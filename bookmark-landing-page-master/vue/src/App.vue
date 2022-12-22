<template>
  <div class="main">
    <Navbar />
    <div class="title-container">
      <div>
        <img src="./assets/images/illustration-hero.svg" alt="image-hero">
      </div>
      <div class="title-section">
        <h1 class="title">A Simple Bookmark Manager</h1>
        <p class="description">A clean and simple interface to organize your favourite websites. Open a new browser tab and see your sites load instantly. Try it for free.</p>
        <div class="btn-section">
          <button class="btn-chrome shadow-sm">Get it on Chrome</button>
          <button class="btn-firefox shadow-md">Get it on Firefox</button>
        </div>
      </div>
    </div>

    <div class="features-container">
      <div class="features-section">
        <div class="features-content">
          <h2>Features</h2>
          <p>Our aim is to make it quick and easy for you to access your favourite websites. Your bookmarks sync between your devices so you can access them on the go.</p>
        </div>
        <ul class="features">
          <li>Simple Bookmarking</li>
          <li>Speedy Searching</li>
          <li>Easy Sharing</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import './scss/main.scss'
import Navbar from './components/Navbar.vue'

export default {
  components: {
    Navbar
  },
  data() {
    return {
      
    }
  },
  methods: {

  }
}
</script>