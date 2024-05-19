<template>
  <div class="main">
    <div class="sidebar">
      <div class="logo">
        <span class="logo-text-bold mr-6">
          <span class="logo-text ">Hai</span>Doc
          <img class="medic-icon" src="../../../../public/Medic.png" alt="" />
        </span>
      </div>
      <div class="components">
        <div class="dashboard">
          <router-link to="dashboard"  href="#">
            <i class="icon ph-bold ph-house"></i>
            <span class="text">Dashboard</span>
          </router-link>
        </div>
        <div class="results">
          <router-link to="/results" href="#">
            <i class="icon ph-bold ph-upload"></i>
            <span class="text">Results</span>
          </router-link>
        </div>
        <div class="settings">
          <router-link to="/settings" >
            <i class="icon ph-bold ph-gear"></i>
            <span class="text">Settings</span>
          </router-link>
        </div>
         <div class="upgrade-plan">
            <div class="upgrade-content">
              <div class="upgrade-text">
                Upgrade Plan Account to use more features
              </div>
              <div class="upgrade-button">
                <div class="button-text">Upgrade Plan</div>
              </div>
            </div>
            <div class="rocket-icon">🚀</div>
          </div>
        <div class="help">
          <router-link to="/help" href="#">
            <i class="icon ph-bold ph-info"></i>
            <span class="text">Get Help</span>
          </router-link>
        </div>
        <div class="logout">
          <router-link to="/logout" >
            <i class="icon ph-bold ph-sign-out"></i>
            <span class="text">Logout</span>
          </router-link>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.main {
  display: flex;
  height: 90vh !important;
  /* background-color: #2C63B0; */
}

.sidebar {
  width: 256px;
  padding: 24px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.logo {
  display: flex;
  justify-content: center;
  align-items: center; /* Add this line to align items in the center */
  margin-bottom: 20px; /* Adjust margin as needed */
}

.logo-text-bold {
  display: flex;
  align-items: center; /* Add this line to align items in the center */
  font-size:35px;
  font-weight: bold;
  color: white;
  /* margin-left: -40px; */
  word-break: keep-all;
  /* margin-bottom: -20px;   */
}

.medic-icon {
  width: 30px;
  height: 30px;
  margin-left: 1px; /* Adjust margin as needed */
  margin-bottom: 25px;
}

.components {
  display: flex;
  flex-direction: column;
  gap: 8px; /* Adjust the gap between components */
  margin-bottom: 200%;
}

.components a {
  display: flex;
  align-items: center;
  gap: 15px; /* Adjust the gap between icon and text */
  color: #CCCCCC;
  text-decoration: none;
  padding: 8px;
  border-radius: 8px;
}

.components a:hover {
background-color: #2C3B4F;
color: white !important;

}

.help, .logout {
  margin-top: 2px; /* Adjust margin as needed */
  /* margin-bottom: 20px; */
}


.help a, .logout a {
  display: flex;
  align-items: center;
  gap: 15px; /* Adjust the gap between icon and text */
  color: #CCCCCC;
  text-decoration: none;
  padding: 8px;
  border-radius: 8px;
}

.help a:hover, .logout a:hover {
  background-color: #2C3B4F;
}

.content {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}


.upgrade-plan {
  width: 186px;
  height: 25vh;
  position: relative;
  margin-top: 43px;
  
}

.upgrade-content {
  width: 90%;
  height: 93%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 20px 14px;
  padding-bottom: 40px;
  background: linear-gradient(99deg, #2AAC95 0%, #1B564B 100%);
  border-radius: 16px;
  overflow: hidden;
}

.upgrade-text {
  color: white;
  font-size: 12px;
  font-family: 'Poppins', sans-serif;
  font-weight: 600;
  text-align: center;
  padding-bottom: 20px;
  padding-top: 40px;
  /* padding: 0 10px; */
}

.upgrade-button {
  width: 140px;
  height: 39px;
  background: #FDFDFD;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
  padding: 3px;
  margin-bottom: 10px;

}

.upgrade-button:hover {
  cursor: pointer;
  transition: ease-in-out;
}

.button-text {
  color: #2AAC95;
  font-size: 12px;
  font-family: 'Poppins', sans-serif;
  font-weight: 600;
  line-height: 18px;
  letter-spacing: 0.20px;
}

.rocket-icon {
  position: absolute;
  top: -66px;
  left: 53%;
  transform: translateX(-50%);
  font-size: 70px;
  color: black;
}

@media (max-width: 768px) {
  .sidebar {
    width: 80px;
  }

  .logo-text-bold {
    font-size: 14px;
  }

  .medic-icon {
    width: 30px;
    height: 30px;
  }

  .components a {
    flex-direction: column;
    padding: 8px;
  }

  .icon {
    font-size: 18px;
  }

  .text {
    font-size: 12px;
  }

  .help, .logout {
    margin-top: 10px;
  }

  .help a, .logout a {
    padding: 8px;
  }

  .upgrade-plan {
    width: 150px;
    height: 200px;
  }

  .upgrade-content {
    padding: 16px 10px;
  }

  .upgrade-text {
    font-size: 10px;
    margin-bottom: 16px;
    margin-top: 32px;
  }

  .upgrade-button {
    width: 140px;
    height: 30px;
    margin-top: 16px;
  }

  .button-text {
    font-size: 10px;
  }

  .rocket-icon {
    font-size: 70px;
    top: -60px;
  }
}
</style>