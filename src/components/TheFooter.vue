<template>
  <div class="footer w-full py-10 bg-white border-t border-gray-300 mt-6 flex flex-col items-center">
    <!-- Logo and Social Icons -->
    <div class="footer-flex-container grid grid-cols-1 md:grid-cols-3 gap-10 md:gap-0 max-w-6xl w-full px-4 md:px-24">
      <div class="flex flex-col items-center md:items-start gap-3">
        <a href="/" class="logo flex items-center mb-5 md:mb-0">
          <span class="logo-text text-base font-normal">Hai</span>
          <span class="logo-text-bold text-base font-bold">Doc</span>
          <img class="medic-icon w-5 h-5 ml-1" src="./icons/Medic.png" alt="Medic Icon" />
        </a>
        <div class="footer-social-icons flex gap-5">
          <img src="./icons/github-142-svgrepo-com.svg" alt="GitHub" class="social-icon w-5 h-5 cursor-pointer" />
          <img src="./icons/linkedin-svgrepo-com.svg" alt="LinkedIn" class="social-icon w-5 h-5 cursor-pointer" />
          <img src="./icons/instagram-167-svgrepo-com.svg" alt="Instagram" class="social-icon w-5 h-5 cursor-pointer" />
        </div>
      </div>

      <!-- Footer Content -->
      <div class="footer-content grid grid-cols-1 md:grid-cols-4 gap-10 md:gap-44 w-full md:w-auto">
        <div class="footer-section flex flex-col gap-4">
          <div class="footer-heading text-gray-900 text-base font-medium">Company</div>
          <div class="footer-links flex flex-col gap-2">
            <router-link to="/" class="text-gray-600 text-base font-medium">Home</router-link>
            <router-link to="/" class="text-gray-600 text-base font-medium">Subscription</router-link>
            <router-link to="/" class="text-gray-600 text-base font-medium">Blog</router-link>
            <router-link to="/" class="text-gray-600 text-base font-medium">Careers</router-link>
          </div>
        </div>
        <div class="footer-section flex flex-col gap-4">
          <div class="footer-heading text-gray-900 text-base font-medium">Products</div>
          <div class="footer-links flex flex-col gap-2">
            <router-link to="/" class="text-gray-600 text-base font-medium">Free</router-link>
            <router-link to="/" class="text-gray-600 text-base font-medium">Plus</router-link>
            <router-link to="/" class="text-gray-600 text-base font-medium">Premium</router-link>
            <router-link to="/" class="text-gray-600 text-base font-medium">Business</router-link>
          </div>
        </div>
        <div class="footer-section flex flex-col gap-4">
          <div class="footer-heading text-gray-900 text-base font-medium">Help Center</div>
          <div class="footer-links flex flex-col gap-2">
            <router-link to="/" class="text-gray-600 text-base font-medium">Privacy Policy</router-link>
            <router-link to="/" class="text-gray-600 text-base font-medium">Terms & Conditions</router-link>
            <router-link to="/" class="text-gray-600 text-base font-medium">Cookies</router-link>
          </div>
        </div>
        <div class="footer-section flex flex-col gap-4">
          <div class="footer-heading text-gray-900 text-base font-medium">Support</div>
          <div class="footer-links flex flex-col gap-2">
            <router-link to="/" class="text-gray-600 text-base font-medium">Help Centre</router-link>
            <router-link to="/" class="text-gray-600 text-base font-medium">Contact us</router-link>
            <router-link to="/" class="footer-email text-gray-600 text-base font-medium underline">Backfeed@yahoo.com</router-link>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-divider w-full h-px bg-gray-300 opacity-30 my-6"></div>
    <div class="footer-copyright text-gray-600 text-sm font-light">
      Copyright © 2024 Backfeed AI. All rights reserved
    </div>
  </div>
</template>

<script>
export default {
  // name: 'Footer'
}
</script>

<style scoped>
/* No scoped styles needed as we are using Tailwind CSS classes */
</style>
