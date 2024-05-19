<script setup>
const scrollToSection = (sectionId) => {
  const section = document.getElementById(sectionId);
  if (section) {
    const scrollOptions = {
      behavior: 'smooth',
      block: 'start' // Scrolls to the top of the target element
    };
    // Smooth scroll to the section
    section.scrollIntoView(scrollOptions);
  }
};
</script>

<template>


  <nav class="w-full h-11 flex justify-between items-center p-4 ">
    <div class="flex items-center gap-2">
      <span class="flex items-center text-blue-900 font-bold text-[20.98px]">
        <span class="text-blue-900 font-medium ml-2">Hai</span>Doc
        <img class="w-[20.98px] h-[20.98px] mr-1 mb-3" src="./icons/Medic.png" alt=""/>
      </span>
    </div>
    <div class="hidden md:flex gap-4">
      <router-link to="/" class="nav-item" :class="{ 'text-green-600': $route.path === '/' }">Home</router-link>
      <router-link to="/about" class="nav-item" :class="{ 'text-green-600': $route.path === '/about' }">About Us</router-link>
      <a href="#team" @click="scrollToSection('team')" class="nav-item" :class="{ 'text-[#31b099]': $route.path === '/team' }">Our Team</a>
      <router-link to="/contact" class="nav-item" :class="{ 'text-green-600': $route.path === '/contact' }">Contact Us</router-link>
    </div>
    <div class="hidden md:flex gap-4 mr-2 mt-1">
      <router-link to="/auth/login" class="auth-button">Log in</router-link>
      <router-link to="/auth/signup" class="auth-button">Sign Up</router-link>
    </div>
    <div class="md:hidden">
      <button @click="toggleMobileMenu" class="text-blue-900 focus:outline-none">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
        </svg>
      </button>
    </div>
  </nav>
  <div v-if="isMobileMenuOpen" class="md:hidden">
    <div class="flex flex-col gap-2 p-4 bg-gray-100">
      <router-link to="/" class="nav-item" :class="{ 'text-green-600': $route.path === '/' }" @click="closeMobileMenu">Home</router-link>
      <router-link to="/about" class="nav-item" :class="{ 'text-green-600': $route.path === '/about' }" @click="closeMobileMenu">About Us</router-link>
      <a href="#team" @click="scrollToSection('team'); closeMobileMenu()" class="nav-item" :class="{ 'text-[#31b099]': $route.path === '/team' }">Our Team</a>
      <router-link to="/contact" class="nav-item" :class="{ 'text-green-600': $route.path === '/contact' }" @click="closeMobileMenu">Contact Us</router-link>
      <router-link to="/auth/login" class="auth-button" @click="closeMobileMenu">Log in</router-link>
      <router-link to="/auth/signup" class="auth-button" @click="closeMobileMenu">Sign Up</router-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isMobileMenuOpen: false
    };
  },
  methods: {
    toggleMobileMenu() {
      this.isMobileMenuOpen = !this.isMobileMenuOpen;
    },
    closeMobileMenu() {
      this.isMobileMenuOpen = false;
    },
    scrollToSection(sectionId) {
      const section = document.getElementById(sectionId);
      if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
      }
    }
  }
};
</script>

<style scoped>
.nav-item {
  @apply px-6 py-2 text-gray-600 text-base font-medium cursor-pointer no-underline;
}

.nav-item:hover {
  @apply text-[#31b099] scale-110 transition-transform duration-300 ease-in-out;
}

.auth-button {
  @apply px-6 py-2 rounded text-black text-sm font-semibold leading-6 cursor-pointer bg-gray-100 no-underline;
}

.auth-button:hover {
  @apply bg-[#31b099] text-white rounded-lg;
}

a.router-link-active {
  @apply text-[#31b099] scale-110 transition-transform duration-300 ease-in-out;
}

@media (max-width: 768px) {
  .nav-item,
  .auth-button {
    @apply text-center w-full;
  }

  .nav-item:hover,
  .auth-button:hover {
    @apply scale-105;
  }
}
</style>
