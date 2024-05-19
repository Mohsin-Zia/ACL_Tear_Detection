<script setup>
import { computed } from 'vue';
import { useRoute } from 'vue-router';
import TheNavbar from './components/TheNavbar.vue';

// Get the current route
const route = useRoute();

// Compute a boolean based on the URL params
const showNavbar = computed(() => {
  return !route.path.includes('/dashboard');
});
</script>

<template>
  <div class="wrapper">
    <div class="navbar" v-if="showNavbar">
      <TheNavbar />
      <nav>
        <!-- <RouterLink to="/"></RouterLink>
        <RouterLink to="/about"></RouterLink>
        <router-link to="/contact"></router-link> -->
      </nav>
    </div>

    <div>
      <!-- <TheDashboard /> -->
    </div>

    <RouterView />
  </div>
</template>

<style scoped>
/* No additional styles needed */
</style>
