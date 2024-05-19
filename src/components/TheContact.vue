<template>
  <div class="contact-container max-w-5xl mx-auto p-5 md:p-10">
    <h1 class="text-4xl font-bold text-center text-black">Contact Us</h1>
    <div class="reach-out-container mt-9 md:mt-12 bg-gradient-to-r from-[#26675b] to-[#2aac95] rounded-3xl overflow-hidden relative p-5 md:p-16">
      <div class="reach-out-content flex flex-col md:flex-row justify-between items-start gap-8 md:gap-0">
        <div class="reach-out-info flex-1 flex flex-col gap-6">
          <h1 class="text-white text-4xl font-bold">Reach Out to Us</h1>
          <p class="text-white text-xl">Ready to boost your digital presence? Let's chat. <br />Your privacy is our priority.</p>
          <div class="contact-info flex flex-col gap-4">
            <div class="contact-item flex items-center gap-2">
              <div class="contact-icon w-7 h-7">
                <img src="./icons/call.png" alt="call" class="w-full h-full" />
              </div>
              <div class="contact-detail text-white text-xl">+92 320 5455789</div>
            </div>
            <div class="contact-item flex items-center gap-2">
              <div class="contact-icon w-7 h-7">
                <img src="./icons/mail.png" alt="mail" class="w-5" />
              </div>
              <div class="contact-detail text-white text-xl">Detection@gmail.com</div>
            </div>
            <div class="contact-item flex items-center gap-2">
              <div class="contact-icon w-7 h-7">
                <img src="./icons/location.png" alt="location" />
              </div>
              <div class="contact-detail text-white text-xl">2A Comsats University, Islamabad</div>
            </div>
          </div>
        </div>
        <form class="form-container flex-1 flex flex-col gap-8" @submit.prevent="submitForm">
          <div class="form-fields flex flex-col gap-6">
            <div class="form-field-row flex flex-col md:flex-row justify-between gap-6">
              <div class="form-field flex flex-col gap-2 w-full">
                <label for="name" class="text-white text-base font-semibold">Your Name</label>
                <div class="input-container bg-white bg-opacity-20 rounded-lg px-4 py-2">
                  <input type="text" id="name" v-model="formData.name" class="bg-transparent w-full text-white outline-none" />
                </div>
              </div>
              <div class="form-field flex flex-col gap-2 w-full">
                <label for="email" class="text-white text-base font-semibold">Your Email</label>
                <div class="input-container bg-white bg-opacity-20 rounded-lg px-4 py-2">
                  <input type="email" id="email" v-model="formData.email" class="bg-transparent w-full text-white outline-none" />
                </div>
              </div>
            </div>
            <div class="form-field-row flex flex-col md:flex-row justify-between gap-6">
              <div class="form-field flex flex-col gap-2 w-full">
                <label for="query" class="text-white text-base font-semibold">Query About?</label>
                <div class="input-container bg-white bg-opacity-20 rounded-lg px-4 py-2">
                  <input type="text" id="query" v-model="formData.query" class="bg-transparent w-full text-white outline-none" />
                </div>
              </div>
              <div class="form-field flex flex-col gap-2 w-full">
                <label for="gender" class="text-white text-base font-semibold">Gender</label>
                <div class="input-container bg-[#4B9E8F] rounded-lg px-4 py-2">
                  <select id="gender" v-model="formData.gender" class="bg-transparent w-full text-white outline-none">
                    <option value="male" class="custom-option">Male</option>
                    <option value="female" class="custom-option">Female</option>
                    <option value="other" class="custom-option">Other</option>
                  </select>
                </div>
              </div>
            </div>
            <div class="form-field flex flex-col gap-2">
              <label for="message" class="text-white text-base font-semibold">Message</label>
              <div class="message-input-container bg-white bg-opacity-20 rounded-lg px-4 py-2 h-32">
                <textarea id="message" v-model="formData.message" class="bg-transparent w-full h-full text-white outline-none"></textarea>
              </div>
            </div>
          </div>
          <button type="submit" class="submit-button bg-gray-100 text-[#2aac95] font-semibold px-5 py-2 rounded-lg hover:bg-gray-200 transition-all">Submit Request</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const formData = ref({
  name: '',
  email: '',
  query: '',
  gender: '',
  message: ''
});

const submitForm = () => {
  console.log("Form Submitted", formData.value);
};

onMounted(() => {
  const options = document.querySelectorAll('#gender option');
  options.forEach(option => {
    option.style.backgroundColor = '#4B9E8F'; // Set your desired background color here
    option.style.color = 'white'; // Set the text color if needed
  });
});
</script>

<style scoped>
/* Additional styles if needed */
</style>
