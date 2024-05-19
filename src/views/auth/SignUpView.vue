<template>
  <div class="flex justify-center items-center h-screen mt-[-25px]">
    <form class="w-[430px] p-5 bg-gray-100 rounded-lg shadow-md flex flex-col items-center gap-8" @submit.prevent="handleSubmit">
      <div class="flex flex-col items-center gap-3">
        <div class="text-gray-800 text-2xl font-bold">Create New Account</div>
        <div class="text-gray-600 text-sm font-semibold">Please register by filling in your personal data</div>
      </div>
      <div class="w-full flex flex-col gap-6">
        <div class="w-full">
          <label for="fullname" class="text-gray-700 text-sm font-semibold">Full Name</label>
          <input type="text" id="fullname" class="w-full h-9 border border-gray-300 rounded-md focus:outline-none" v-model="fullName" />
        </div>
        <div class="w-full">
          <label for="email" class="text-gray-700 text-sm font-semibold">Email</label>
          <input type="email" id="email" class="w-full h-9 border border-gray-300 rounded-md focus:outline-none" v-model="email" />
        </div>
        <div class="w-full">
          <label for="password" class="text-gray-700 text-sm font-semibold">Password</label>
          <input type="password" id="password" class="w-full h-9 border border-gray-300 rounded-md focus:outline-none" v-model="password" />
        </div>
        <!-- <div class="w-full">
          <label for="userType" class="text-gray-700 text-sm font-semibold">User Type</label>
          <select id="userType" class="w-full h-9 border border-gray-300 rounded-md focus:outline-none" v-model="userType">
            <option value="player">Player</option>
            <option value="admin">Admin</option>
          </select>
        </div> -->
      </div>
      <div class="w-full">
      <button class="w-full h-12 bg-[#31b099] text-white font-bold rounded-md cursor-pointer">Sign up</button>
      </div>
      <div class="w-full text-center text-red-500 font-semibold" v-if="hasError">{{ error }}</div>
      <div class="w-full text-center text-green-500 font-semibold" v-if="successMessage">{{ successMessage }}</div>
      <div class="flex justify-center items-center gap-2">
        <span class="text-gray-600 text-sm">Already have an account?</span>
        <RouterLink to="/auth/login" class="text-[#31b099] text-sm font-bold cursor-pointer">Login</RouterLink>
      </div>
    </form>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const fullName = ref('');
const email = ref('');
const password = ref('');
const userType = ref('player'); // Default value set to 'player'
const error = ref(null);
const successMessage = ref('');

const handleSubmit = async () => {
  // Reset error and success message
  error.value = null;
  successMessage.value = '';

  // Validate full name
  if (!fullName.value.trim()) {
    error.value = 'Please enter your full name.';
    return;
  }

  // Validate email
  const emailRegex = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;
  if (!emailRegex.test(email.value)) {
    error.value = 'Please enter a valid email address.';
    return;
  }

  // Validate password
  if (password.value.length < 8) {
    error.value = 'Password must be at least 8 characters long.';
    return;
  }

  const user = {
    userName: fullName.value, 
    email: email.value,
    password: password.value,
    userType: userType.value // Include the selected user type in the user object
  };

  try {
    const response = await fetch("http://localhost:8800/api/auth/signup", {
      method: "POST",
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify(user)
    });

    if (response.ok) {
      const json = await response.json();
      fullName.value = '';
      email.value = '';
      password.value = '';
      successMessage.value = `user successfully created an account!`;
      setTimeout(() => {
        successMessage.value = '';
      }, 4000);
    } else {
      const json = await response.json();
      error.value = json.message;
      console.error('Error adding user:', json);
    }
  } catch (error) {
    console.error('Error adding user:', error);
    error.value = 'An error occurred while adding the user.';
  }
};

const hasError = computed(() => error.value !== null);
</script>
