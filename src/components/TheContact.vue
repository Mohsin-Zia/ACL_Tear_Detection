<template>
  <div class="contact-container">
    <h1 class="text-4xl font-bold">Contact Us</h1>
  <div class="reach-out-container">
    <div class="reach-out-content">
      <div class="reach-out-info">
        <h1>Reach Out to Us</h1>
        <p>
          Ready to boost your digital presence? Let's chat. <br />
          Your privacy is our priority.
        </p>
        <div class="contact-info">
          <div class="contact-item">
            <div class="contact-icon"> <img src="./icons/call.png" alt=""> </div>
            <div class="contact-detail">+92 320 5455789</div>
          </div>
          <div class="contact-item">
            <div class="contact-icon"> <img src="./icons/mail.png" style="width:22px" alt=""> </div>
            <div class="contact-detail">Detection@gmail.com</div>
          </div>
          <div class="contact-item">
            <div class="contact-icon"><img src="./icons/location.png" alt="location"  /></div>
            <div class="contact-detail">2A Comsats university, Islamabad</div>
          </div>
        </div>
      </div>
      <form class="form-container">
        <div class="form-fields">
          <div class="form-field-row">
            <div class="form-field">
              <label for="name">Your Name</label>
              <div class="input-container">
                <input type="text" id="name" v-model="formData.name" />
              </div>
            </div>
            <div class="form-field">
              <label for="email">Your Email</label>
              <div class="input-container " >
                <input type="email" id="email" v-model="formData.email"  />
              </div>
            </div>
          </div>
          <div class="form-field-row">
            <div class="form-field">
              <label for="query">Query About?</label>
              <div class="input-container">
                <input type="text" id="query" v-model="formData.query" />
              </div>
            </div>
            <div class="form-field">
              <label for="gender">Gender</label>
              <div class="input-container">
                <select id="gender" style="background-color: #4B9E8F;" v-model="formData.gender" >
                  <option value="male" >Male</option>
                  <option value="female">Female</option>
                  <option value="other">Other</option>
                </select>
              </div>
            </div>
          </div>
          <div class="form-field">
            <label for="message">Message</label>
            <div class="message-input-container">
              <textarea id="message" v-model="formData.message"></textarea>
            </div>
          </div>
        </div>
        <button class="submit-button" @click="submitForm">Submit Request</button>
      </form>
    </div>
  </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        name: '',
        email: '',
        query: '',
        gender: '',
        message: ''
      }
    }
  },
  methods: {
    submitForm() {
      // Handle form submission here
      console.log('Form submitted:', this.formData)
    }
  }
}
</script>

<style scoped>
.contact-container {
  max-width: 1210px;
  margin: 0 auto;
  padding: 20px;
  margin-top: -15px;
  margin-left: 40px;
}

h1 {
  text-align: center;
  color: black;
}
.reach-out-container {
  margin-top: 35px;
  margin-left: 23px;
  width: 1210px;
  height: 500px;
  position: relative;
  background: linear-gradient(90deg, #26675b 0%, #2aac95 100%);
  border-radius: 32px;
  overflow: hidden;
}

label {
  color: white;
}

img {
  width: 19px;
  height: 20px;
  margin-top: 2px;
}

.reach-out-content {
  position: absolute;
  left: 64px;
  top: 64px;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
}

.reach-out-info {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  gap: 24px;
}

.reach-out-info h1 {
  color: white;
  font-size: 40px;
  font-family: Inter;
  font-weight: 700;
  word-wrap: break-word;
}

.reach-out-info p {
  width: 432px;
  color: white; /* Changed to white */
  font-size: 20px;
  font-family: Inter;
  font-weight: 500;
  line-height: 20px;
  word-wrap: break-word;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 8px;
}

.contact-detail {
  color: white; /* Changed to white */
  font-size: 20px;
  font-family: General Sans;
  font-weight: 500;
  line-height: 32px;
  word-wrap: break-word;
}

.contact-icon {
  width: 28px;
  height: 28px;
  position: relative;
}

.contact-form {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  gap: 24px;
}

.contact-form input,
.contact-form textarea {
  width: 319px;
  height: 48px;
  background: rgba(255, 255, 255, 0.16);
  border-radius: 12px;
  padding: 0 16px;
  color: white; /* Changed to white */
  font-size: 14px;
  font-family: Inter;
  font-weight: 500;
  line-height: 20px;
  border: none; /* Removed border */
  outline: none;
}

.contact-form input:focus,
.contact-form textarea:focus {
  outline: none; /* Remove outline when focused */
}

.form-container {
  width: 672px;
  height: 507px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-end;
  gap: 32px;
}

.form-fields {
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.form-field {
  display: flex;
  flex-direction: column;
  gap: 12px;

}

.label {
  color: white;
  font-size: 16px;
  font-family: Inter;
  font-weight: 600;
  line-height: 24px;
  word-wrap: break-word;
}

  .input-container {
    width: 319px;
    padding: 14px;
    background: rgba(255, 255, 255, 0.16);
    border-radius: 12px;
    border: none;
    background-color: #4B9E8F;
  }

.message-input-container {
  width: 650px;
  padding: 14px;
  background: rgba(255, 255, 255, 0.16);
  border-radius: 12px;
}

input,
select,
textarea {
  width: 100%;
  border: none;
  background: none;
  color: white; 
  font-size: 14px;
  font-family: Inter;
  font-weight: 500;
  line-height: 20px;
  word-wrap: break-word;
  outline: none;
}

.form-field-row {
  display: flex;
  justify-content: space-between;
}

.form-field {
  width: calc(50% - 12px); 
   
}

.submit-button {
  width: auto;
  padding: 14px 20px;
  background: #fafafa;
  border-radius: 12px;
  color: #2aac95;
  font-size: 16px;
  font-family: Poppins;
  font-weight: 600;
  line-height: 24px;
  word-wrap: break-word;
  border: none;
}

.submit-button:hover {
  background: rgb(235, 233, 233);
  /* color: white; */
  cursor: pointer;
  transition: all 0.4s ease-in-out;
}

</style>
