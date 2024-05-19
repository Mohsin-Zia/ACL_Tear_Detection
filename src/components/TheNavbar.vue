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
  <nav class="w-full h-11 flex justify-between items-center">
    <div class="flex items-center gap-2">
      <span class="flex items-center text-blue-900 font-bold text-[20.98px]">
        <span class="text-blue-900 font-medium ml-2">Hai</span>Doc
        <img class="w-[20.98px] h-[20.98px] mr-1 mb-3" src="./icons/Medic.png" alt=""/>
      </span>
    </div>
    <div class="flex gap-4">
      <router-link to="/" class="nav-item" :class="{ 'text-green-600': $route.path === '/' }">Home</router-link>
      <router-link to="/about" class="nav-item" :class="{ 'text-green-600': $route.path === '/about' }">About Us</router-link>
      <a href="#team" @click="scrollToSection('team')" class="nav-item" :class="{ 'text-[#31b099]': $route.path === '/team' }">Our Team</a>
      <router-link to="/contact" class="nav-item" :class="{ 'text-green-600': $route.path === '/contact' }">Contact Us</router-link>
    </div>
    <div class="flex gap-4 mr-2 mt-1">
      <router-link to="/auth/login" class="auth-button">Log in</router-link>
      <router-link to="/auth/signup" class="auth-button">Sign Up</router-link>
    </div>
  </nav>
</template>

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
 a.router-link-active{
    @apply text-[#31b099] scale-110 transition-transform duration-300 ease-in-out;
}
</style>
