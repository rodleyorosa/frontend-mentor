<template>
  <div class="features-container">
      <div class="features-section">
        <div class="features-content features-content1 text-center">
          <h2>Features</h2>
          <p>Our aim is to make it quick and easy for you to access your favourite websites. Your bookmarks sync between your devices so you can access them on the go.</p>
        </div>
        <ul class="features text-center">
          <li
          :class="{'feature-selected': featureSelected == 1}"
          @click="selectFeature(1)">Simple Bookmarking</li>
          <li
          :class="{'feature-selected': featureSelected == 2}"
          @click="selectFeature(2)">Speedy Searching</li>
          <li
          :class="{'feature-selected': featureSelected == 3}"
          @click="selectFeature(3)">Easy Sharing</li>
        </ul>
        <div v-for="(feature, id) in features" :key="id">
          <div
          v-show="featureSelected == (id + 1)"
          class="features-tabs">
            <div>
              <img class="m-auto" :src="require(`../assets/images/${feature.img}.svg`)" alt="">
            </div>
            <div class="features-content features-content2">
              <h2>{{ feature.title }}</h2>
              <p>{{ feature.description }}</p>
              <button class="btn-chrome shadow-sm">More info</button>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  props: [
    'featureSelected',
    'features'
  ],
  methods: {
    selectFeature(id) {
      this.$emit('selectFeature', id)
    }
  }
}
</script>

<style>
  li.feature-selected {
    border-bottom: 5px solid #fa5757;
  }
</style>