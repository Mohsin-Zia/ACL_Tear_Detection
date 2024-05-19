<template>
  <div class="container">
    <div class="left-side">
      <div class="logo">
        <div class="logo-text">
          <span class="hai">Hai</span><span class="doc">Doc</span>
        </div>
        <div class="logo-icon">
          <img src="../../../public/Medic.png" alt="" width="30px" height="30px" style="margin-bottom: 3px" />
        </div>
      </div>
      <div class="nav">
        <div class="nav-item">
          <router-link to="/dashboard" class="nav-link">Dashboard</router-link>
        </div>
        <div class="nav-item">
          <router-link to="/results" class="nav-link">Results</router-link>
        </div>
        <div class="nav-item">
          <router-link to="/exercises" class="nav-link">Exercises</router-link>
        </div>
        <div class="nav-item active">
          <router-link to="/settings" class="nav-link">Settings</router-link>
        </div>
      </div>
    </div>
    <div class="right-side">
      <div class="search">
        <div class="search-icon">
          <div class="icon-inner"></div>
        </div>
        <div class="search-input">Search anything here</div>
      </div>
      <div class="notification">
        <div class="notification-icon">
          <div class="icon-inner"></div>
        </div>
      </div>
      <div class="profile">
        <img src="../../assets/ehsan.jpg" alt="Profile" class="profile-image" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TopBar'
}
</script>

<style scoped>
.container {
  width: 100%;
  padding: 20px 60px;
  background: #1C2536;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.left-side {
  display: flex;
  align-items: center;
  gap: 40px;
}

.logo {
  width: 80px;
  height: 32px;
  position: relative;
}

.logo-text {
  position: absolute;
  left: 0;
  top: 7.83px;
  text-align: center;
}

.hai {
  color: #FAFAFA;
  font-size: 16px;
  font-family: 'Poppins';
  font-weight: 500;
}

.doc {
  color: #FAFAFA;
  font-size: 16px;
  font-family: 'Poppins';
  font-weight: 700;
}

.logo-icon {
  width: 30px;
  height: 30px;
  position: absolute;
  left: 50px;
  top: 0;
}

.nav {
  display: flex;
  align-items: center;
  gap: 10px;
}

.nav-item {
  padding: 10px 20px;
  border-radius: 10px;
}

.nav-link {
  font-size: 12px;
  text-decoration: none;
  color: #A2A6AA;
}

.active {
  background: #333B4A;
}

.active .nav-link {
  color: #FAFAFA;
  font-weight: 700;
}

.right-side {
  display: flex;
  align-items: center;
  gap: 14px;
}

.search {
  width: 268px;
  height: 40px;
  padding: 0 18px;
  background: rgba(255, 255, 255, 0.07);
  border-radius: 100px;
  display: flex;
  align-items: center;
  gap: 16px;
}

.search-icon {
  width: 20px;
  height: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.search-input {
  color: rgba(255, 255, 255, 0.50);
  font-size: 12px;
  font-family: 'Satoshi';
  font-weight: 500;
}

.notification {
  width: 40px;
  height: 40px;
  background: rgba(255, 255, 255, 0.07);
  border-radius: 100px;
  display: inline-flex;
  justify-content: center;
  align-items: center;
}

.notification-icon {
  width: 20px;
  height: 20px;
}

.profile {
  display: flex;
  align-items: center;
  gap: 6px;
}

.profile-image {
  width: 40px;
  height: 40px;
  border-radius: 9999px;
  border: 5px solid #2C3542;
}

@media (max-width: 768px) {
  .container {
    padding: 10px 20px;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }

  .left-side {
    gap: 20px;
  }

  .logo {
    width: 60px;
    height: 24px;
  }

  .logo-icon {
    width: 24px;
    height: 24px;
    left: 40px;
  }

  .nav-item {
    padding: 8px 16px;
    border-radius: 8px;
  }

  .nav-link {
    font-size: 10px;
  }

  .search {
    width: 200px;
    height: 32px;
  }

  .search-icon {
    width: 16px;
    height: 16px;
  }

  .search-input {
    font-size: 10px;
  }

  .notification {
    width: 32px;
    height: 32px;
  }

  .notification-icon {
    width: 16px;
    height: 16px;
  }

  .profile-image {
    width: 32px;
    height: 32px;
    border: 3px solid #2C3542;
  }
}
</style>