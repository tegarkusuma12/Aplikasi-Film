<template>
  <div id="app">
    <!-- Navbar -->
    <NavBar />
    <!-- Navbar -->
    <!-- isi web -->
    <div class="container">
      <transition name="fade">
        <router-view/>
      </transition>
    </div>
    <!-- isi web -->
  </div>
</template>

<script>
  import NavBar from '@/components/NavBar.vue';

  export default {
    name: "App",
    components: {
      NavBar,
    },
  }
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
