

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
  <section
    id="contact"
    style="background-image: url('https://themewagon.gitlab.io/restaurant/assets/img/food/green.png');
           background-repeat: no-repeat;
           height: 700px;
           animation: slide-bg 10s linear infinite;" 
    class="block1 bg-gray-50 h-[700px] w-full animate-on-scroll">
    <div class="slide-in-bottom">
      <center>
        <p class="font-mono text-2xl pt-[120px] text-opacity-70">Location & Timings</p>
      </center>
    </div>
    <div class="slide-in-bottom">
      <center>
        <h2 class="font-serif font-bold pt-2 text-4xl">Contact with us</h2>
      </center>
    </div>
    <br><br><br>
    <div class="disp flex flex-col md:flex-row justify-between items-center pt-12 h-auto md:h-80 w-full px-5 md:px-[80px] space-y-8 md:space-y-0">
      <div class="h-[230px] w-full md:w-[350px] bg-white rounded-md justify-center px-4 py-6 sm:shadow-lg md:shadow-lg">
        <p class="font-mono text-md text-gray-500">Av. Paz Soldán 290, San <br>Isidro, Lima 27 - Peru</p><br>
        <p class="font-mono text-sm text-gray-500">+511 442-2777</p><br>
        <p class="font-mono text-sm text-gray-500">mail@restaurantpro.com</p>
      </div>
      <div class="h-[230px] w-full md:w-[350px] bg-white rounded-md px-4 py-6 sm:shadow-lg md:shadow-lg">
        <p class="font-bold text-red-600 text-opacity-70">Hours of service</p><br>
        <p class="font-medium font-sans text-md">Monday to Saturday</p>
        <p class="font-mono text-md text-gray-500">1:00 pm - 3:00 pm and <br>7:00 pm - 11:00 pm</p><br>
        <p class="font-medium font-sans text-md">Sunday</p>
        <p class="font-mono text-md text-gray-500">12:30 pm - 3:30 pm</p>
      </div>
      <div
        class="h-[230px] w-full md:w-[350px] bg-white rounded-md sm:shadow-lg md:shadow-lg"
        style="background-image: url('https://themewagon.gitlab.io/restaurant/assets/img/food/kisspng-soup.png');
               background-position: top right;
               background-repeat: no-repeat;
               background-size: 150px 150px;
               animation: zoom-bg 6s ease-in-out infinite;
               padding-right: 50px;">
        <p class="font-bold text-gray-700 font-sans text-md pt-[50px] pl-4">Telephone support:</p>
        <p class="font-sans text-gray-600 text-md pl-4">Monday to Saturday from <br>9:00 am to 9:00 pm</p>
        <br>
        <button class="bg-red-400 text-gray-800 py-2 px-10 rounded-md cursor-pointer font-bold hover:bg-red-500 font-sans text-opacity-70 ml-4">
          MAKE A RESERVATION
        </button>
      </div>
    </div>
  </section>
</template>

<style scoped>

/* Initial state for animation */
.animate-on-scroll {
  opacity: 0;
  transform: translateX(50px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}

/* Animated state */
.animate-on-scroll.animate {
  opacity: 1;
  transform: translateX(0);
}

/* Keyframes for sliding the background */
@keyframes slide-bg {
  0% {
    background-position: top left;
  }
  50% {
    background-position: center center;
  }
  100% {
    background-position: bottom right;
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

/* Keyframes for zooming the background */
@keyframes zoom-bg {
  0% {
    background-size: 150px 150px;
  }
  50% {
    background-size: 200px 200px;
  }
  100% {
    background-size: 150px 150px;
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
        animation-timeline: view();
        animation-range: entry 0% cover 40%;
      }

@media (max-width: 769px) {
  #contact {
    height: 2000px;
    background-size: 100%;
    background-image: none;    
  }
  .disp {
    display: flex;
    flex-direction: column;
  }
  .px-4 {
    padding-left: 20px;
    padding-right: 20px;
  }
  .font-serif {
    font-size: 1.5rem;
  }
  .font-mono {
    font-size: 0.9rem;
  }
}
</style>
