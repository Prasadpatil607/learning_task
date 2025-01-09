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
    { threshold: 0.7 } // Trigger when 25% of the element is visible
  );

  animatedElements.forEach((el) => observer.observe(el));
});
</script>

<template>
  <section class="block1 h-auto w-full bg-gray-100">
    <div class="w-full px-4 py-6 md:px-6 md:py-8 bg-white shadow-lg rounded-md ">
      <!-- Heading Section -->
      <h1 class="slide-in-bottom text-2xl md:text-3xl font-medium font-serif text-center mb-4 mt-12 md:mt-[80px] animate-on-scroll">
        Feel free to drop us a line!
      </h1>
      <p class="slide-in-bottom text-sm md:text-base text-center font-mono text-gray-600 mb-6 animate-on-scroll">
        Let's talk if you have any query or suggestion. We are open to learn from you. <br>
        So don't hesitate to reach us anytime.
      </p>

      <!-- Form Section -->
      <form class="flex flex-col md:flex-row pt-6 md:pt-[50px] space-y-6 md:space-y-0 md:space-x-6">
        <!-- Left Column -->
        <div class="h-auto md:h-[300px] w-full md:w-[50%]">
          <div class="mb-4">
            <input
              type="text"
              id="name"
              class="w-full px-4 py-2 font-mono border border-gray-300 rounded-md focus:ring-2 focus:ring-yellow-300 focus:outline-none"
              placeholder="Your Name" required
            />
          </div>
          <div class="mb-4">
            <input
              type="text"
              id="subject"
              class="w-full px-4 py-2 font-mono border border-gray-300 rounded-md focus:ring-2 focus:ring-yellow-300 focus:outline-none"
              placeholder="Subject" required
            />
          </div>
          <div class="mb-4">
            <input
              type="email"
              id="email"
              class="w-full px-4 py-2 font-mono border border-gray-300 rounded-md focus:ring-2 focus:ring-yellow-300 focus:outline-none"
              placeholder="Email Address" required
            />
          </div>
          <div class="mb-4 flex items-center">
            <input
              type="checkbox"
              id="copy"
              class="h-4 w-4 accent-yellow-400 border-gray-300 rounded"
            />
            <label for="copy" class="ml-2 font-serif text-sm md:text-md text-gray-700  focus:ring-yellow-300">
              Send me a copy
            </label>
          </div>
        </div>

        <!-- Right Column -->
        <div class="h-auto md:h-[300px] w-full md:w-[50%]">
          <div class="mb-4">
            <textarea
              id="message"
              class="w-full px-4 py-2 font-mono border border-gray-300 rounded-md focus:ring-2 focus:ring-yellow-300 focus:outline-none"
              placeholder="Type your message here" required
              rows="4"
            ></textarea>
          </div>
          <div class="flex justify-center md:justify-start">
            <button class="bg-gray-900 text-gray-100 py-2 px-6 md:px-10 rounded-md cursor-pointer font-medium hover:bg-black font-sans text-opacity-70">
              GIVE US A SHOT
            </button>
          </div>
        </div>
      </form>
    </div>
  </section>
</template>
<style scoped>
/* Initial state for animation */
.animate-on-scroll {
  opacity: 0;
  transform: translateY(50px);
  transition: opacity 0.8s ease-out 1s, transform 0.8s ease-out 1s;
}

/* Animated state */
.animate-on-scroll.animate {
  opacity: 1;
  transform: translateY(0);
}

@keyframes zoomIn {
      0% {
        transform: scale(0.5); /* Start smaller */
        opacity: 0;           /* Fully transparent */
      }
      100% {
        transform: scale(1);  /* Normal size */
        opacity: 1;           /* Fully visible */
      }
    }
    .zoom-in {
      display: inline-block;     
      animation: zoomIn 0.8s ease-out; 
      animation-delay: 1.5s;             
      animation-fill-mode: both;   
    }

    
</style>
