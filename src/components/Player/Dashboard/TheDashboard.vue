<script setup>
import DashboardItem from './DashboardItem.vue';
import TheSidebar from './TheSidebar.vue';
import TheCentered from './TheCentered.vue';

</script>
<template>
  <div class="h-screen flex body overflow-x-hidden">
    <DashboardItem>
      <template #sidebar>
        <div class="w-[20%] h-[60%] fixed top-0 left-0">
          <TheSidebar/>
        </div>
      </template>

      <template #mainDashboard>
        <div class="ml-64 p-4 h-screen w-[63%] rounded-xl fixed top-0 left-0">
          <TheCentered/>
        </div>
      </template>
    </DashboardItem>
  </div>
</template>


<style scoped>
.body {
  background-color: #1C2634;
/* Add this line to make the body a positioning context */
}


</style>