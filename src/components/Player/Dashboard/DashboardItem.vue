<template >
    <div class="dashboardItem">
    <!-- <slot name="navbar"></slot> -->
    <!-- <div class="flex flex-row"> -->

    <slot name="sidebar" > this is default sidebar</slot>
    <slot name="mainDashboard"> this is default main dashboard screen</slot>
    <!-- </div> -->
  </div>
</template>