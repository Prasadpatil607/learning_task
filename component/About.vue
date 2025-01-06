<script setup>
import { onMounted } from "vue";

onMounted(() => {
  const animatedElements = document.querySelectorAll(".animate-on-scroll");

  const observer = new IntersectionObserver(
    (entries, observer) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("animate");
          observer.unobserve(entry.target); // Unobserve to trigger only once
        }
      });
    },
    { threshold: 0.25 } // Trigger when 25% of the element is visible
  );

  animatedElements.forEach((el) => observer.observe(el));
});
</script>

<template>
  <section class=" ml-[80px] relative animate-on-scroll">
    <!-- Section Heading -->
    <div class="block1 text-center sm:text-left">
      <p class="slide-in-bottom font-mono text-2xl pt-7 text-opacity-70">About Us</p>
    </div>
    <div class="block1 text-center sm:text-left">
      <h2 class="slide-in-bottom font-serif font-bold text-3xl">Who Are We?</h2>
      <p class="slide-in-bottom2 pt-5 text-gray-500 text-sm font-mono font-medium leading-relaxed text-base">
        We are a chain of theme restaurant founded in 1971 in London. In <br>1979, the cafe began covering its walls with rock and roll <br>memorabilia, a tradition which expanded to others in the chain.
      </p>
    </div>
    <br>
    <button class="bg-yellow-400 text-gray-800 py-2 px-10 rounded-md cursor-pointer font-bold hover:bg-yellow-500 font-sans text-opacity-70">
      LEARN MORE
    </button>

    <div class="block1 w-full mt-8">
      <div class="slide-in-right grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 p-2 py-4 lg:w-[700px]" >
        <!-- Image Cards -->
        <div class="image_card overflow-hidden flex flex-col items-center">
          <img src="https://themewagon.gitlab.io/restaurant/assets/img/team/1.png" alt="" class="rounded-full max-w-[70%] h-auto">
          <p class="text-white-400 font-bold text-md font-mono px-4">Gordon Ramsey</p>
          <p class="text-white-50 font-mono text-md text-opacity-80 px-4 text-sm">Owner & Founder</p>
        </div>
        <div class="image_card overflow-hidden flex flex-col items-center">
          <img src="https://themewagon.gitlab.io/restaurant/assets/img/team/2.png" alt="" class="rounded-full max-w-[70%] h-auto">
          <p class="text-white-400 font-bold text-md font-mono px-4">Gordon Ramsey</p>
          <p class="text-white-50 font-mono text-md text-opacity-80 px-4 text-sm">Owner & Founder</p>
        </div>
        <div class="image_card overflow-hidden flex flex-col items-center">
          <img src="https://themewagon.gitlab.io/restaurant/assets/img/team/3.png" alt="" class="rounded-full max-w-[70%] h-auto">
          <p class="text-white-400 font-bold text-md font-mono px-4">Gordon Ramsey</p>
          <p class="text-white-50 font-mono text-md text-opacity-80 px-4 text-sm">Owner & Founder</p>
        </div>
        <div class="image_card overflow-hidden flex flex-col items-center">
          <img src="https://themewagon.gitlab.io/restaurant/assets/img/team/4.png" alt="" class="rounded-full max-w-[70%] h-auto">
          <p class="text-white-400 font-bold text-md font-mono px-4">Gordon Ramsey</p>
          <p class="text-white-50 font-mono text-md text-opacity-80 px-4 text-sm">Owner & Founder</p>
        </div>
        <div class="image_card overflow-hidden flex flex-col items-center">
          <img src="https://themewagon.gitlab.io/restaurant/assets/img/team/5.png" alt="" class="rounded-full max-w-[70%] h-auto">
          <p class="text-white-400 font-bold text-md font-mono px-4">Gordon Ramsey</p>
          <p class="text-white-50 font-mono text-md text-opacity-80 px-4 text-sm">Owner & Founder</p>
        </div>
        <div class="image_card overflow-hidden flex flex-col items-center">
          <img src="https://themewagon.gitlab.io/restaurant/assets/img/team/6.png" alt="" class="rounded-full max-w-[70%] h-auto">
          <p class="text-white-400 font-bold text-md font-mono px-4">Gordon Ramsey</p>
          <p class="text-white-50 font-mono text-md text-opacity-80 px-4 text-sm">Owner & Founder</p>
        </div>
      </div>
    </div>
    
    <!-- Background Section -->
    <div class=" bg-holder"></div>
  </section>
</template>

<style scoped>

/* Initial state for animation */
.animate-on-scroll {
  opacity: 0;
  transform: translateX(-50px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}

/* Animated state */
.animate-on-scroll.animate {
  opacity: 1;
  transform: translateX(0);
}
.bg-holder {
  background-image: url(https://themewagon.gitlab.io/restaurant/assets/img/food/soup.png);
  background-position: right center;
  background-size: 40%;
  transform: matrix(1, 0, 0, 1, 0, 0);
  position: absolute;
  width: 100%;
  min-height: 100%;
  top: 0;
  left: 0;
  overflow: hidden;
  will-change: transform, opacity, filter;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  background-repeat: no-repeat;
  z-index: -1;
}

.slide-in-bottom {
  transform: translateY(50px);
  opacity: 0;
  animation: slideInBottom 1s forwards;
}

@keyframes slideInBottom {
  0% {
    transform: translateY(50px);
    opacity: 0;
  }
  100% {
    transform: translateY(0);
    opacity: 1;
  }
}

.slide-in-bottom2 {
  transform: translateY(50px);
  opacity: 0;
  animation: slideInBottom 3s forwards;
}

@keyframes slideInBottom {
  0% {
    transform: translateY(50px);
    opacity: 0;
  }
  100% {
    transform: translateY(0);
    opacity: 1;
  }
}

.image_card {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.slide-in-right {
  transform: translateX(50px);
  opacity: 0;
  animation: slideInRight 1s forwards;
}


@keyframes slideInRight {
  0% {
    transform: translateX(-50px);
    opacity: 0;
  }
  100% {
    transform: translateX(0);
    opacity: 1;
  }
}

.slide-in-left {
  transform: translateX(50px);
  opacity: 0;
  animation: slideInLeft 2s forwards;
}

@keyframes slideInLeft {
  0% {
    transform: translateX(50px);
    opacity: 0;
  }
  100% {
    transform: translateX(0);
    opacity: 1;
  }
}

/* Mobile responsiveness */
@media (max-width: 768px) {
  /* Change the number of columns in the grid on smaller screens */
  .grid-cols-1 {
    grid-template-columns: 1fr;
  }

  .sm\:grid-cols-2 {
    grid-template-columns: repeat(2, 1fr);
  }

  .text-center {
    text-align: center;
  }

  /* Padding adjustments for smaller devices */
  .w-full {
    width: 100%;
    padding-left: 10px;
    padding-right: 10px;
  }

  .font-mono {
    font-size: 1.1rem;
  }
  .bg-holder {
    display: none;
  }
}

@media (max-width: 480px) {
  .font-serif {
    font-size: 1.5rem;
  }
}
</style>
