<template>
  <section class="h-auto">
    <div class="p-8 flex flex-col lg:flex-row gap-4">
      <!-- Large image on the left for larger screens -->
      <div class="bg-white bg-opacity-80 rounded lg:w-[50%]">
        <img 
          src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/bigimg.jpg" 
          class="rounded w-full h-[420px] cursor-pointer hover:shadow-2xl transition-all duration-400" 
          alt="img1"
        >
      </div>

      <!-- Smaller images on the right -->
      <div class="grid grid-cols-3 grid-rows-2 gap-4 lg:grid-cols-3 lg:w-[50%]">
        <div class="bg-white bg-opacity-80 text-center">
          <img 
            src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/1.jpg" 
            alt="img2" 
            class="rounded h-[200px] w-[200px] cursor-pointer hover:shadow-2xl transition-all duration-400"
          >
        </div>
        <div class="bg-white bg-opacity-80 text-center">
          <img 
            src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/2.jpg" 
            alt="img3" 
            class="rounded h-[200px] w-[200px] cursor-pointer hover:shadow-2xl transition-all duration-400"
          >
        </div>
        <div class="bg-white bg-opacity-80 text-center">
          <img 
            src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/3.jpg" 
            alt="img4" 
            class="rounded h-[200px] w-[200px] cursor-pointer hover:shadow-2xl transition-all duration-400"
          >
        </div>
        <div class="bg-white bg-opacity-80 text-center">
          <img 
            src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/4.jpg" 
            alt="img5" 
            class="rounded h-[200px] w-[200px] cursor-pointer hover:shadow-2xl transition-all duration-400"
          >
        </div>
        <div class="bg-white bg-opacity-80 text-center">
          <img 
            src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/5.jpg" 
            alt="img6" 
            class="rounded h-[200px] w-[200px] cursor-pointer hover:shadow-2xl transition-all duration-400"
          >
        </div>
        <div class="bg-white bg-opacity-80 text-center">
          <img 
            src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/6.jpg" 
            alt="img7" 
            class="rounded h-[200px] w-[200px] cursor-pointer hover:shadow-2xl transition-all duration-400"
          >
        </div>
      </div>
    </div>
  </section>
</template>
