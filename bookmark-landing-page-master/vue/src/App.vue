<template>
  <div class="main">
    <Navbar />
    <TitleSection />
    <Features
    :featureSelected="featureSelected"
    :features="features"
    @selectFeature="selectFeature"/>
    <Extension />
    <Questions />
    <ContactUs />
    <Footer />
  </div>
</template>

<script>
import './scss/main.scss'
import Navbar from './components/Navbar.vue'
import Features from './components/Features.vue'
import TitleSection from './components/TitleSection.vue'
import Extension from './components/Extension.vue'
import Questions from './components/Questions.vue'
import Footer from './components/Footer.vue'
import ContactUs from './components/ContactUs.vue'

export default {
  components: {
    Navbar,
    Features,
    TitleSection,
    Extension,
    Questions,
    Footer,
    ContactUs
  },
  data() {
    return {
      featureSelected: 1,
      features: [
        {
          id: 1,
          title: 'Bookmark in one click',
          description: 'Organize your bookmarks however you like. Our simple drag-and-drop interface gives you complete control over how you manage your favourite sites.',
          img: 'illustration-features-tab-1'
        },
        {
          id: 2,
          title: 'Intelligent search',
          description: 'Our powerful search feature will help you find saved sites in no time at all. No need to trawl through all of your bookmarks.',
          img: 'illustration-features-tab-2'
        },
        {
          id: 3,
          title: 'Share your bookmarks',
          description: 'Easily share your bookmarks and collections with others. Create a shareable link that you can send at the click of a button.',
          img: 'illustration-features-tab-3'
        }
      ]
    }
  },
  methods: {
    selectFeature(id) {
      this.featureSelected = id
    }
  }
}
</script>
