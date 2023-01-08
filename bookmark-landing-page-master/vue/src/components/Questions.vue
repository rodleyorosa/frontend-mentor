<template>
  <div class="features-container">
    <div class="features-section">
      <div class="features-content m-auto">
        <div class="text-center">
          <h2>Frequently Asked Questions</h2>
          <p>Here are some of our FAQs. If you have any other questions you’d like answered please feel free to email us.</p>
        </div>
        <div
        v-for="(faq, id) in faqs" :key="id"
        class="question-container my-10">
          <div
          @click="open(id)"
          class="question-title flex items-center justify-between">
            <h3>{{ faq.question }}</h3>
            <img
            v-show="faq.isOpened"
            src="../assets/images/icon-arrow.svg" alt="arrow">
            <img
            v-show="!faq.isOpened"
            class="rotate-180" src="../assets/images/icon-arrow.svg" alt="arrow">
          </div>
          <div v-show="faq.isOpened">
            <p>
              {{ faq.answer }}
            </p>
          </div>
        </div>
        <div class="text-center">
        <button class="btn-chrome question-btn">More info</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      faqs: [
        {
          id: 1,
          question: 'What is Bookmark?',
          answer: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce tincidunt justo eget ultricies fringilla. Phasellus blandit ipsum quis quam ornare mattis.',
          isOpened: false
        },
        {
          id: 2,
          question: 'How can I request a new browser?',
          answer: 'Vivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non ligula. Suspendisse imperdiet. Vivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non ligula. Suspendisse imperdie tVivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non ligula. Suspendisse imperdiet.',
          isOpened: false
        },
        {
          id: 3,
          question: 'Is there a mobile app?',
          answer: 'Sed consectetur quam id neque fermentum accumsan. Praesent luctus vestibulum dolor, ut condimentum urna vulputate eget. Cras in ligula quis est pharetra mattis sit amet pharetra purus. Sed sollicitudin ex et ultricies bibendum.',
          isOpened: false
        },
        {
          id: 4,
          question: 'What about other Chromium browsers?',
          answer: 'Integer condimentum ipsum id imperdiet finibus. Vivamus in placerat mi, at euismod dui. Aliquam vitae neque eget nisl gravida pellentesque non ut velit.',
          isOpened: false
        },
      ]
    }
  },
  methods: {
    open(id) {
      if( this.faqs[id].isOpened == false) {
        this.faqs[id].isOpened = true
      } else {
        this.faqs[id].isOpened = false
      }
    }
  }
}
</script>

<style>
.question-title {
  cursor: pointer;
}
.question-title:hover {
  color: #fa5757;
}
</style>