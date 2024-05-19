<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';

const email = ref('');
const password = ref('');
const error = ref(null);
const router = useRouter();

const handleSignIn = async () => {
  const userCredentials = {
    email: email.value,
    password: password.value
  };

  try {
    const response = await fetch("http://localhost:8800/api/auth/login", {
      method: "POST",
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify(userCredentials)
    });

    if (response.ok) {
      // Redirect to about page upon successful login
      router.push('/dashboard');
    } else {
      const json = await response.json();
      error.value = json.message;
      console.error('Login failed:', json);
    }
  } catch (error) {
    console.error('Error during login:', error);
    error.value = 'An error occurred during login.';
  }
};
</script>

<template>
  <div class="flex justify-center items-center h-screen mt-[-25px]">
    <form class="w-[430px] p-5 bg-[#F4F4F7] rounded-2xl shadow-md flex flex-col items-center gap-8" @submit.prevent="handleSignIn">
      <div class="flex flex-col items-center gap-3">
        <div class="text-[#1a1c1e] text-2xl font-bold">Login to Your Account</div>
      </div>
      <div class="w-full flex flex-col gap-6">
        <div class="w-full">
          <label for="email" class="text-[#676767] text-sm font-bold">Email</label>
          <input type="email" id="email" class="w-full h-9 border border-[#dce4e8] rounded-md focus:border-gray-300 focus:outline-none" v-model="email" />
        </div>
        <div class="w-full">
          <label for="password" class="text-[#676767] text-sm font-bold">Password</label>
          <input type="password" id="password" class="w-full h-9 border border-[#dce4e8] rounded-md focus:border-gray-300 focus:outline-none" v-model="password" />
        </div>
      </div>
      <div class="flex justify-between items-center w-full">
        <div class="flex items-center gap-2">
          <input type="checkbox" id="rememberMe" v-model="rememberMe" />
          <label for="rememberMe" class="text-[#1a1c1e] text-sm font-bold">Remember me</label>
        </div>
        <div class="text-[#31b099] text-sm font-bold cursor-pointer">Forgot Password</div>
      </div>
      <!-- <button class="w-full h-12 bg-[#31b099] text-white font-bold rounded-md cursor-pointer">Login</button> -->
      <div class="flex flex-col items-center gap-4">

         <button class="w-full h-12 bg-[#31b099] text-white font-bold rounded-md cursor-pointer ">Login
         </button>
        <button class="w-full h-12 flex items-center justify-center bg-white border border-[#e0e0e0] rounded-md text-[#333333] font-medium cursor-pointer transition duration-300 p-3">
          <img src="../../components/icons/google.png" alt="Google Icon" class="w-6 h-6 mr-3" />
          Continue with Google
        </button>
        <!-- <button class="w-full h-12 flex items-center justify-center bg-white border border-[#e0e0e0] rounded-md text-[#333333] font-medium cursor-pointer transition duration-300">
          <img src="../../components/icons/logos_facebook.png" alt="Facebook Icon" class="w-6 h-6 mr-3" />
          Continue with Facebook
        </button> -->
      </div>
      <div class="flex justify-center items-center gap-2">
        <div>Don’t have an account?</div>
        <RouterLink to="/auth/signup" class="text-[#31b099] text-sm font-bold cursor-pointer">Register Here</RouterLink>
      </div>
    </form>
  </div>
</template>
