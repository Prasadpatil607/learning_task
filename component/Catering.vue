<template>
  <section class="block1">
    <!-- Heading Section -->
    <div class="text-center">
      <p class="slide-in-bottom head font-mono text-2xl pt-7 text-opacity-70">Catering</p>
      <h2 class="slide-in-bottom font-serif font-bold text-4xl mt-2">We Manage Your Events</h2>
      <p class="zoom-in headp pl-5 pt-5 text-gray-500 text-sm font-mono font-medium leading-relaxed mt-5 text-base">
        Allow our Chef to deliver the perfect private dinner or cocktail party experience in your <br>home; or let us simply add a little extra flavor to your next office meeting, boat trip, or <br>beach picnic. By partnering with our sibling location Rosewater Wine & Spirits, we can <br>offer a full array of bar services and beverage selections. Email us to learn more.
      </p>
    </div>
    <br><br><br>

    <div class="flex justify-center items-center flex-wrap">
      <div class="w-full md:w-[600px] h-auto md:h-60 rounded-md shadow-lg flex flex-col md:flex-row justify-center items-center hover:shadow-xl transition-all duration-300 p-4">
        <!-- Image Section -->
        <div class="h-40 w-40 md:w-60 md:h-60">
          <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/pancake_PNG94.png" alt="Catering Image" class="" />
        </div>

        <!-- Text and Button Section -->
        <div class="mt-4 md:mt-0 text-center md:text-left">
          <p class="font-bold text-opacity-70 text-gray-900">We Cater in Weddings,<br>Corporate Functions <br>and Events</p><br>
          <button class="bg-yellow-400 text-gray-800 py-2 px-10 rounded-md cursor-pointer hover:bg-yellow-500 font-sans text-opacity-70">
            HIRE US NOW
          </button>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>

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

    /* Apply the animation to the element */
    .zoom-in {
      display: inline-block;     /* For better handling of inline elements */
      animation: zoomIn 0.8s ease-out; /* Animation duration and timing */
      animation-delay: 1.5s;              /* Delay before animation starts */
      animation-fill-mode: both;   
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

@keyframes appear {
        from {
          opacity: 0;
          clip-path: inset(100% 100% 0 0);
        }
        to {
          opacity: 1;
          clip-path: inset(0 0 0 0);
        }
      }

      .block1 {
        animation: slideInBottom 1s forwards;
        animation: zoomIn 0.8s ease-out;
        animation-timeline: view();
        animation-range: entry 0% cover 40%;
      }
  @media screen and (max-width: 330px) {
    h2{
      font-size: 1.3rem;
    }
    .head{
      font-size: 1rem;
    }
  }
</style>