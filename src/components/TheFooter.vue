<template>
  <div class="footer">
    <!-- Logo -->
    
    <div class="footer-flex-container">
      <div class="flex">
        <a href="/" class="logo">
      <span class="logo-text">Hai</span><span class="logo-text-bold">Doc</span>
      <img class="medic-icon" src="./icons/Medic.png" alt="" />
    </a>
      <!-- Social Icons -->
      <div class="footer-social-icons">
        <img src="./icons/github-142-svgrepo-com.svg" alt="GitHub" class="social-icon text-3xl text-white hover:cursor-pointer " />
        <img src="./icons/linkedin-svgrepo-com.svg" alt="LinkedIn" class="social-icon text-3xl text-white hover:cursor-pointer" />
        <img src="./icons/instagram-167-svgrepo-com.svg" alt="Instagram" class="social-icon text-3xl text-white hover:cursor-pointer" />
      </div>
      </div>
   
      
      <!-- Footer Content -->
      <div class="footer-content">
        <div class="footer-section">
          <div class="footer-heading">Company</div>
          <div class="footer-links">
            <div> <router-link to="/"> Home</router-link> </div>
            <div>Subscription</div>
            <div>Blog</div>
            <div>Careers</div>
          </div>
        </div>
        <div class="footer-section">
          <div class="footer-heading">Products</div>
          <div class="footer-links">
            <div>Free</div>
            <div>Plus</div>
            <div>Premium</div>
            <div>Business</div>
          </div>
        </div>
        <div class="footer-section">
          <div class="footer-heading">Help Center</div>
          <div class="footer-links">
            <div>Privacy Policy</div>
            <div>Terms & Conditions</div>
            <div>Cookies</div>
          </div>
        </div>
        <div class="footer-section">
          <div class="footer-heading">Support</div>
          <div class="footer-links">
            <div>Help Centre</div>
            <div>Contact us</div>
            <div class="footer-email">Backfeed@yahoo.com</div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-divider"></div>
    <div class="footer-copyright">Copyright © 2024 Backfeed AI. All rights reserved</div>
  </div>
</template>

<script>
export default {
  // name: 'Footer'
}
</script>

<style scoped>
.footer {
  width: 100%;
  padding: 40px 0;
  background: white;
  border-top: 1px solid #b1b1b1;
  border-left: 0;
  border-right: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 23px;
}

.footer-flex-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1440px;
  width: 100%;
  padding: 0 100px;
  gap: 10px; /* Reduce the gap */
  margin-left: 120px; /* Adjust the margin to start from left edge */
}

.flex {
  display: flex; /* Enable flexbox layout */
  flex-direction: column; /* Stack items vertically */
  align-items: center; /* Center items horizontally */
  gap: 3px; /* Adjust the gap between logo and icons */
}

.logo {
  display: flex;
  align-items: center;
  float: left; /* Float the logo to the left */
  margin-bottom: 20px; /* Adjust the margin as needed */
  text-decoration: none
}

.logo-text {
  font-size: 16px;
  font-family: Poppins;
  font-weight: 400;
}

.logo-text-bold {
  font-size: 16px;
  font-family: Poppins;
  font-weight: 700;
}

.medic-icon {
  width: 20px;
  height: 20px;
  margin-left: 5px;
}

.footer-social-icons {
  display: flex;
  gap: 20px;
}

.social-icon {
  width: 20px;
  height: 20px;
}

.footer-content {
  display: flex;
  gap: 90px;
  margin-right: 70px;
}

.footer-section {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.footer-heading {
  color: #0b0e1a;
  font-size: 16px;
  font-family: Poppins;
  font-weight: 500;
  line-height: 28px;
}

.footer-links {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.footer-links div {
  color: #979797;
  font-size: 16px;
  font-family: Poppins;
  font-weight: 500;
  line-height: 28px;
}

.footer-email {
  text-decoration: underline;
}

.footer-divider {
  width: 100%;
  height: 1px;
  opacity: 0.3;
  background-color: #b1b1b1;
  margin: 24px 0;
}

.footer-copyright {
  color: #979797;
  font-size: 14px;
  font-family: Poppins;
  font-weight: 400;
  line-height: 20px;
}
</style>
