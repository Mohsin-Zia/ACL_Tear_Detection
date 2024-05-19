<script setup>
import WelcomeItem from './WelcomeItem.vue'
// import TheNavbar from './TheNavbar.vue'
import MainContent from './MainContent.vue'
import TheFooter from './TheFooter.vue'
</script>


<template>
  <div>
    <!-- The header/Nvabar -->
    <welcome-item>
      <!-- <template #navbar>
        <TheNavbar />
      </template> -->
      <template #main>
        <MainContent />
      </template>

      <template #footer>
        <TheFooter />
      </template>

    </welcome-item>
    
  </div>
</template>