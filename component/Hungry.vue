<template>
  <section class="bg bg-black h-65 flex justify-center items-center flex-col md:flex-row">
    <!-- Image Section - Hidden on Mobile -->
    <div class="block1 slide-in-bottom h-80 w-90 md:block hidden">
      <img
        class="mt-[-95px] relative animate-on-scroll"
        src="https://themewagon.gitlab.io/restaurant/assets/img/food/fried-clipart-transparent-background-7.png"
        alt="img"
        height="350"
        width="350"
      />
    </div>

    <!-- Text Section -->
    <div class="bg-yellow h-30 w-80 ml-[30px] mt-[40px] md:mt-0 md:ml-0 flex flex-col justify-center items-center md:items-start">
      <p class="text-yellow-400 font-bold text-md font-mono">Hungry?</p>
      <h1 class="text-white font-serif font-bold text-xl">We will home deliver!</h1><br />
      <button
        class="bg-yellow-400 text-gray-800 py-2 px-10 rounded-md cursor-pointer hover:bg-yellow-500 font-sans font-medium text-opacity-70"
      >
        MAKE AN ORDER
      </button>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from "vue";

onMounted(() => {
  const animatedSections = document.querySelectorAll(".animate-on-scroll");

  const observer = new IntersectionObserver(
    (entries, observer) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("animate");
          observer.unobserve(entry.target); // Unobserve to trigger the animation only once
        }
      });
    },
    { threshold: 0.5 } // Trigger when 50% of the element is visible
  );

  animatedSections.forEach((section) => observer.observe(section));
});
</script>

<style scoped>
/* Initial State for Animation */
.animate-on-scroll {
  opacity: 0;
  transform: translateY(50px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}

/* Animation Triggered State */
.animate-on-scroll.animate {
  opacity: 1;
  transform: translateY(0);
}

@media (max-width: 330px) {
  .bg {
    width: 100%;
  }
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
</style>
