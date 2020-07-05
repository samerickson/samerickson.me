<template>
  <div id="app">
    <NavBar />
    <div class="content">
      <router-view/>
    </div>
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from '@/components/NavBar.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'Home',
  components: {
    NavBar,
    Footer,
  },
};
</script>

<style scoped>
 .content {
   min-height: 90vh;
 }
</style>
