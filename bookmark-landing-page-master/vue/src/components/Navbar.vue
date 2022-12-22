<template>
  <nav class="my-10 flex justify-between">
    <a href="#">
      <img src="../assets/images/logo-bookmark.svg" alt="logo">
    </a>
    <div class="nav-desktop">
      <div class="nav-section items-center">
        <p class="nav-elements"><a href="#">features</a></p>
        <p class="nav-elements"><a href="#">pricing</a></p>
        <p class="nav-elements"><a href="#">contact</a></p>
        <a href="#" class="btn-login">login</a>
      </div>
    </div>
    <div class="nav-mobile">
      <img class="cursor-pointer" @click.prevent="isMenuActive != isMenuActive" src="../assets/images/icon-hamburger.svg" alt="hamburger">
      <div>
        
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isMenuActive: false
    }
  },
  console() {

  }
}
</script>