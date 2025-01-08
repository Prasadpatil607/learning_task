
<script>
export default {
  data() {
    return {
      isLoaded: false, // Initially false to show the preloader
    };
  },
  mounted() {
    // Simulate loading time
    setTimeout(() => {
      this.isLoaded = true; // Hide preloader after 2 seconds
    }, 3500);
  },
};
</script>


<template>
    <div id="app">
  <div class="preloader" v-bind:class="{ loaded: isLoaded }">
    <div><img src="../assets/egg.gif" alt=""></div>
  </div>
  <main v-show="isLoaded">
    <router-view></router-view>
  </main>
</div>

</template>

<style scoped>
    .preloader {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 10001;
  background-color: #fd6061;
  opacity: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: opacity 2s cubic-bezier(0.77, 0, 0.18, 1);
}

.preloader.loaded {
  opacity: 0;
  pointer-events: none;
}

</style>