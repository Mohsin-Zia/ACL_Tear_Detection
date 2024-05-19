<script setup>
import OurTeam from './OurTeam.vue'
import ContactUsView from '../views/ContactView.vue'
import { useRouter } from 'vue-router';

// initilizse the router
const router = useRouter()

const handleDemoRequest = () => {
  router.push('/auth/signup')
}
</script>

<template>
  <div>
    <div class="centered-container">
      <div class="gradient-background">
        <div class="rotated-rectangles">
          <!-- Rotated rectangles -->
        </div>
        <div class="main-content">
          <!-- Main content -->
          <div class="title">Precision ACL Detection for Enhanced Recovery and Performance</div>
          <div class="description">
            Precision ACL Detection for Enhance Utilize our state-of-the-art web application to
            swiftly identify anterior cruciate ligament (ACL) injuries with unparalleled accuracy.
          </div>
          <div class="button-container">
            <div class="button" @click="handleDemoRequest">
              <div class="button-icon">
                <!-- Button icon -->
                <img class="icon" src="./icons/playIcon.png" alt="Play Icon" />
              </div>
              <div class="button-label">Request Demo</div>
            </div>
          </div>
        </div>
        <div class="kneeImg">

        <img class="image" src="./icons/KneeeInjured.png" alt="Demo Image" />
        </div>
      </div>
    </div>
    <div>

      <div class="health-care-solutions">
        <div class="health-care-title">Health Care Solutions</div>
        <div class="health-care-description">
          Precision ACL Detection for Enhanced Utilization. Use our state-of-the-art web application
          to swiftly identify anterior cruciate ligament (ACL) injuries with unparalleled accuracy.
        </div>
        <div class="features">
          <div class="feature">
            <div class="health-care-icon">
              <div class="circle">💪</div>
              <div class="text">Strengthening</div>
            </div>
          </div>
          <div class="feature">
            <div class="health-care-icon">
              <div class="circle">🤸‍♀️</div>
              <div class="text">Flexibility</div>
            </div>
          </div>
          <div class="feature">
            <div class="health-care-icon">
              <div class="circle">🏋️‍♂️</div>
              <div class="text">Technique</div>
            </div>
          </div>
          <div class="feature">
            <div class="health-care-icon">
              <div class="circle">🦵</div>
              <div class="text">Support</div>
            </div>
          </div>
          <div class="feature">
            <div class="health-care-icon">
              <div class="circle">📚</div>
              <div class="text">Education</div>
            </div>
          </div>
        </div>
      </div>

      <div class="ourteam" id="team">
        <OurTeam />
      </div>

      <div>
        <ContactUsView />
      </div>
    </div>
  </div>
</template>
  

  
<style scoped>
.centered-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin-top: -70px;
}

.gradient-background {
  width: auto;
  max-width: 90%;
  position: relative;
  background: linear-gradient(90deg, #1e6a5c 0%, #176859 100%),
    linear-gradient(0deg, rgba(0, 0, 0, 0.3) 0%, rgba(0, 0, 0, 0.3) 100%);
  border-radius: 16px;
  overflow: hidden;
  display: flex;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
}

.main-content {
  padding: 60px;
  position: relative;
  text-align: center;
  flex: 1;

}

.health-care-solutions {
  width: 90%;
  max-width: 1124px;
  height: auto;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  gap: 20px; /* Reduce the gap between sections */
  margin: -55px auto 80px; /* Adjust margin to shift towards the top */
}

.title {
  font-size: 32px;
  font-weight: 700;
  margin-bottom: 16px;
}

.description {
  font-size: 18px;
  font-weight: 500;
  margin-bottom: 24px;
}

.button-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.button {
  display: flex;
  align-items: center;
  background: white;
  border-radius: 8px;
  padding: 12px 24px;
  cursor: pointer;
  margin-left: 25px;
  margin-top: 5px;
  transition: transform 0.1s ease;
  animation: moveButton 2s infinite alternate; /* Adjust the duration */
}

@keyframes moveButton {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(8px);
  }
  100% {
    transform: translateY(0);
  }
}

.button:hover {
  transform: translateY(-5px);
}

.button-label {
  color: #2aac95;
  font-size: 16px;
  font-weight: bold;
  margin-left: 10px;
}

.icon {
  width: 24px;
  height: 24px;
}
.kneeImg {
  display: flex;
  justify-content: center;
  align-items: center;
  
}

.image {
  width: 250px;
  height: 250px;
  margin: 15px 15px 15px 15px;
}

.health-care-title {
  text-align: center;
  color: #0b0e1a;
  font-size: 32px;
  font-weight: 700;
}

.health-care-description {
  opacity: 0.9;
  text-align: center;
  color: #979797;
  font-size: 18px;
  font-weight: 500;
  line-height: 1.6;
  margin-top: -20px;
}

.features {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  flex-wrap: wrap;
  gap: 40px;
}

.feature {
  width: 180px;
  height: auto;
  position: relative;
  background: #f6f7fb;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0px 4px 10px rgba(106, 103, 103, 0.2);
  transition: transform 0.3s ease;
}

.feature:hover {
  transform: translateY(-10px);
  cursor: pointer;
}

.health-care-icon {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
}

.circle {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 80px;
  height: 80px;
  background: white;
  border-radius: 50%;
  font-size: 40px;
  font-weight: 800;
}

.text {
  color: black;
  font-size: 16px;
  margin-top: 10px;
}

@media (max-width: 768px) {
  .centered-container {
    height: auto;
    margin-top: 0;
  }

  .gradient-background {
    flex-direction: column;
  }

  .main-content {
    padding: 40px;
  }

  .title {
    font-size: 24px;
  }

  .description {
    font-size: 16px;
  }


  .health-care-solutions {
    margin: 40px auto;
  }

  .health-care-title {
    font-size: 24px;
  }

  .health-care-description {
    font-size: 16px;
  }

  .features {
    gap: 20px;
  }

  .feature {
    width: 150px;
  }

  .circle {
    width: 60px;
    height: 60px;
    font-size: 32px;
  }

  .text {
    font-size: 14px;
  }
}
</style>