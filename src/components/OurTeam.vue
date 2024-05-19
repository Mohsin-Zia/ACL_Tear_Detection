<script setup>
import { ref } from 'vue';
import ehsanImage from '../assets/ehsan.jpg';
// import sirJunaidImage from '../assets/sirJunaid.jpeg';
import moizImage from '../assets/moiz.jpg';
import instaIcon from "../components/icons/instagram-167-svgrepo-com.svg";
import githubIcon from "../components/icons/github-142-svgrepo-com.svg";
import emailIcon from "../components/icons/email-svgrepo-com.svg";
import linkedinIcon from "../components/icons/linkedin-svgrepo-com.svg";


const teamMembers = ref([
  {
    name: 'Ehsan Ahmed',
    role: 'Web Developer',
    image: ehsanImage,
    bio: 'Crafting pixels with purpose, code that dances, and experiences that captivate. Web development is where creativity meets interactivity.',
    links: [
      { url: 'https://www.instagram.com/', icon: instaIcon, alt: 'Instagram' },
      { url: 'https://github.com/', icon: githubIcon, alt: 'GitHub' },
      { url: 'mailto:example@example.com', icon: emailIcon, alt: 'Email' },
      { url: 'https://www.linkedin.com/', icon: linkedinIcon, alt: 'LinkedIn' }
    ]
  },
  // {
  //   name: 'Mr. Junaid Ali',
  //   role: 'Supervisor',
  //   image: sirJunaidImage,
  //   bio: 'Crafting pixels with purpose, code that dances, and experiences that captivate. Web development is where creativity meets interactivity.',
  //   links: [
  //     { url: 'https://www.instagram.com/', icon: instaIcon, alt: 'Instagram' },
  //     { url: 'https://github.com/', icon: githubIcon, alt: 'GitHub' },
  //     { url: 'mailto:example@example.com', icon: emailIcon, alt: 'Email' },
  //     { url: 'https://www.linkedin.com/', icon: linkedinIcon, alt: 'LinkedIn' }
  //   ]
  // },
  {
    name: 'Abdul Moiz',
    role: 'Android Developer',
    image: moizImage,
    bio: 'From lines of code to touches of magic, Android development blends innovation and user delight into small, yet impactful experiences.',
    links: [
      { url: 'https://www.instagram.com/', icon: instaIcon, alt: 'Instagram' },
      { url: 'https://github.com/', icon: githubIcon, alt: 'GitHub' },
      { url: 'mailto:example@example.com', icon: emailIcon, alt: 'Email' },
      { url: 'https://www.linkedin.com/', icon: linkedinIcon, alt: 'LinkedIn' }
    ]
  }
]);
</script>


<template>
  <div class="team-container">
    <div class="team-header">
      <div class="team-header-title">Our Team</div>
      <div class="team-header-description">
        Precision ACL Detection for Enhance Utilize our state-of-the-art web application to swiftly
        identify anterior cruciate ligament (ACL) injuries with unparalleled accuracy.
      </div>
    </div>
    <div class="team-members">
      <div v-for="(member, index) in teamMembers" :key="index" class="team-member">
        <div class="team-member-card">
          <div class="team-member-indicator"></div> <!-- Indicator added -->
          <div class="team-member-info">
            <div class="team-member-name">{{ member.name }}</div>
            <div class="team-member-role">{{ member.role }}</div>
          </div>
          <img :src="member.image" :alt="member.name" class="team-member-image" />
          <div class="team-member-bio">
            <div class="bio-text">{{ member.bio }}</div>
            <div class="bio-icons">
              <a v-for="(link, i) in member.links" :key="i" :href="link.url" target="_blank">
                <img :src="link.icon" :alt="link.alt" />
                <!-- <img :src="require(`../icons/${link.icon}`)" :alt="link.alt" /> -->

              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<style scoped>
.team-container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.team-header {
  text-align: center;
  margin-bottom: 40px;
}

.team-header-title {
  font-size: 40px;
  font-weight: bold;
  color: #0b0e1a;
}

.team-header-description {
  font-size: 20px;
  color: #979797;
  line-height: 1.5;
}

.team-members {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.team-member {
  width: 300px;
  margin: 20px;
  /* gap: 20px; */
}

.team-member-card {
  position: relative;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  transition: transform 0.8s ease;
  margin-top: 10px;
}

.team-member-card:hover {
  transform: translateY(-5px);
  cursor: pointer;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
}

.team-member-indicator {
  width: 40.5px;
  height: 110.5px;
  font-weight: bold;
  /* left: 50%; */
  right:  1px;
  /* top:  10px; */
  transform: translateX(-20%);
  position: absolute;
  border-radius: 100px;
  border: 3px #2aac95 dotted;
  top: -65.5px;
}

.team-member-info {
  padding: 20px;
}

.team-member-name {
  font-size: 24px;
  font-weight: bold;
  color: #0b0e1a;
  margin-bottom: 5px;
}

.team-member-role {
  font-size: 20px;
  color: #979797;
}

.team-member-image {
  width: 100%;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}

.team-member-bio {
  background-color: #2aac95;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
  padding: 20px;
  /* margin-bottom: -10px ; */
}

.bio-text {
  font-size: 14px;
  color: #fff;
  line-height: 1.5;
  margin-bottom: 10px;
}

.bio-icons {
  display: flex;
  justify-content: center;
  align-items: center;
}

.bio-icons a {
  margin-right: 10px;
}

.bio-icons img {
  width: 30px;
  height: 30px;
  filter: grayscale(100%);
  transition: filter 0.3s ease;
}

.bio-icons img:hover {
  filter: grayscale(0%);
}
</style>
