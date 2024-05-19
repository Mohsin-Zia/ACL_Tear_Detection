<template>
  <div class="main bg-white w-[128%] h-[101%] mb-4 rounded-2xl shadow-lg flex flex-col overflow-hidden">
    <div class="navbar flex flex-col w-full p-5 border-b border-gray-200">
      <!-- Header container -->
      <div class="header-container flex justify-between items-center">
        <div class="title text-[#12182A] text-xl font-medium">Upload MRI</div>
        <div class="search-bar flex items-center bg-gray-100 rounded-3xl shadow-sm p-2">
          <div class="search-icon text-gray-100 mr-2">
            <i class="fas fa-search text-[#1f1f20a1]"></i>
          </div>
          <input class="search-text border-none outline-none bg-transparent text-[#12182A] text-sm gap-4" placeholder="  search anything here"/>
        </div>
        <div class="user-info flex items-center mr-9">
          <div class="user-avatar">
            <img src="../../../assets/ehsan1.jpg" alt="User Avatar" class="rounded-full w-10 h-10"/>
          </div>
          <div class="user-details ml-2.5">
            <div class="user-name text-[#202020] text-sm font-medium">Ehsan Ahmed</div>
            <div class="user-role text-gray-400 text-xs">Admin - Backfeed.Ai</div>
          </div>
        </div>
      </div>
    </div>

    <div class="main-content flex">
      <div class="sidebar w-1/5 bg-gray-100 flex flex-col p-5 rounded-2xl mt-4 ml-2 h-max">
        <!-- Upload MRI section -->
        <div class="nav-item flex items-center p-4 mb-2.5 rounded-lg cursor-pointer transition duration-300 ease-in-out text-black hover:text-white hover:bg-[#31B099]">
          <i class="fas fa-upload mr-2.5"></i>
          <span class="text-sm font-medium">Upload MRI</span>
        </div>
        <!-- Results section -->
        <div class="nav-item flex items-center p-4 mb-2.5 rounded-lg cursor-pointer transition duration-300 ease-in-out hover:text-white hover:bg-gray-300">
          <i class="fas fa-check-circle mr-2.5"></i>
          <span class="text-sm font-medium">Results</span>
        </div>
      </div>

      <div class="content-area w-4/5 p-5">
        <!-- Back button -->
        <div class="back-button flex items-center text-[#12182A] text-sm font-medium cursor-pointer mb-5">
          <i class="fas fa-arrow-left mr-1.5"></i>
          <span>Back</span>
        </div>

        <!-- Upload MRI Section -->
        <div class="upload-section flex flex-col">
          <h4 class="upload-title text-[#12182A] text-lg font-medium mb-5">Upload MRI <i class="fas fa-info-circle text-gray-400"></i></h4>
          <div class="uploadMri bg-white p-10 rounded-2xl flex justify-center items-center border border-dotted border-[#31B099] mb-5">
            <div class="upload-container flex flex-col items-center text-center">
              <div class="upload-icon text-4xl text-[#187D7E] mb-5">
                <i class="fas fa-upload"></i>
              </div>
              <div class="upload-text">
                <span class="drag-drop text-sm font-semibold">Drag & drop files or </span>
                <span class="browse text-[#187D7E] text-sm font-semibold underline cursor-pointer">Browse</span>
              </div>
              <div class="format-info text-xs text-gray-500 mt-2.5">
                <span>Supported formats will be .npy, .pc, .pck. Maximum 1 Images</span>
              </div>
            </div>
          </div>
          <div class="action-buttons flex justify-end">
            <button class="cancel-button bg-white text-black border border-[#187D7E] rounded-lg px-5 py-2.5 text-sm cursor-pointer mr-2.5">Cancel</button>
            <button class="yes-button bg-[#31B099] text-white rounded-lg px-5 py-2.5 text-sm cursor-pointer w-[10.5%]">Yes</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css');
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600&display=swap');

body {
  @apply font-[Poppins] bg-[#f4f4f4] m-0 p-0 flex justify-center items-center h-screen;
}

.nav-item.active {
  @apply bg-[#187D7E] text-white;
}

.nav-item:hover {
  @apply bg-[#31B099];
}

.nav-item {
  @apply rounded-lg cursor-pointer transition duration-300 ease-in-out;
}

</style>
