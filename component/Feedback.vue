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

const slides = ref([
{
          feed: "Restaurant Pro probably make one of the best pizza in Town. I would definitely post their pizza picture someday. But today I have tasted their another items. So there I have mentioned that",
          title: "-lily rose",
         
        },
        
        {
          feed:"hicoiojecmi iwjc oiweqjcj oefjcoijeoijcoidc joce jcoi jrejco jcoiqewjocij qpcoiqj ",
          title: "-Noha Kingon",
          
        },
        {
            feed:"am thrilled with the possibilities that Slick brought to my web design agency. Creating is easier with Slick.",
            title:"-Noha Kingon"
        },
        {
          feed:"Restaurant & Cafe, we aim at promoting the foodstuff industry through the branches , we establish and through the new dishes. and integrate between different cultures, by merging different Oriental and its western recipes",
          title:"-Richard Henriks"
        }
])

const currentIndex = ref(0);
  
      const nextSlide = () => {
        currentIndex.value =
          (currentIndex.value + 1) % slides.value.length; // Loop to the first slide
      };
  
      const prevSlide = () => {
        currentIndex.value =
          (currentIndex.value - 1 + slides.value.length) % slides.value.length; // Loop to the last slide
      };
  
      const goToSlide = (index) => {
        currentIndex.value = index;
      };
  
      // return { slides, currentIndex, nextSlide, prevSlide, goToSlide };
  
</script>

<template>
  <section class=" h-auto w-full flex flex-col md:flex-row items-center md:items-start">
    <!-- Text Content Section -->
    <div class="h-auto md:h-[300px] w-full md:w-[600px] md:ml-[320px] justify-center space-y-2 text-center">
      <center>
        <svg
          class="svg-inline--fa fa-quote-left fa-w-16 mb-2 h-4 w-4 text-gray-500"
          aria-hidden="true"
          data-prefix="fas"
          data-icon="quote-left"
          role="img"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 512 512"
        >
          <path
            fill="currentColor"
            d="M464 256h-80v-64c0-35.3 28.7-64 64-64h8c13.3 0 24-10.7 24-24V56c0-13.3-10.7-24-24-24h-8c-88.4 0-160 71.6-160 160v240c0 26.5 21.5 48 48 48h128c26.5 0 48-21.5 48-48V304c0-26.5-21.5-48-48-48zm-288 0H96v-64c0-35.3 28.7-64 64-64h8c13.3 0 24-10.7 24-24V56c0-13.3-10.7-24-24-24h-8C71.6 32 0 103.6 0 192v240c0 26.5 21.5 48 48 48h128c26.5 0 48-21.5 48-48V304c0-26.5-21.5-48-48-48z"
          ></path>
        </svg>
      </center>
    
      <center>
        <div id="star" class="h-auto w-full flex justify-center text-red-400 space-x sm:h-2 md:h-2 lg:h-4">
          <svg
            class="svg-inline--fa fa-star fa-w-18"
            aria-hidden="true"
            data-prefix="fas"
            data-icon="star"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 576 512"
          >
            <path
              fill="currentColor"
              d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z"
            ></path>
          </svg>
          <svg
            class="svg-inline--fa fa-star fa-w-18"
            aria-hidden="true"
            data-prefix="fas"
            data-icon="star"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 576 512"
          >
            <path
              fill="currentColor"
              d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z"
            ></path>
          </svg>
          <svg
            class="svg-inline--fa fa-star fa-w-18"
            aria-hidden="true"
            data-prefix="fas"
            data-icon="star"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 576 512"
          >
            <path
              fill="currentColor"
              d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z"
            ></path>
          </svg>
          <svg
            class="svg-inline--fa fa-star fa-w-18"
            aria-hidden="true"
            data-prefix="fas"
            data-icon="star"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 576 512"
          >
            <path
              fill="currentColor"
              d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z"
            ></path>
          </svg>
          <svg
            class="svg-inline--fa fa-star fa-w-18"
            aria-hidden="true"
            data-prefix="fas"
            data-icon="star"
            role="img"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 576 512"
          >
            <path
              fill="currentColor"
              d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z"
            ></path>
          </svg>
        </div>
      </center>
      <center>
        <!-- <p class="font-mono text-gray-500 mt-2">
          "Restaurant & Cafe, we aim at promoting the foodstuff <br />
          industry through the branches , we establish and <br />
          through the new dishes. and integrate between different <br />
          cultures, by merging different Oriental and its western <br />
          recipes"
        </p> -->



        <div class="slider-container">
      <!-- Slider Wrapper -->
      <div
        class="slider-wrapper"
        :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
      >
        <div
          v-for="(slide, index) in slides"
          :key="index"
          class="slide"
          :style="{ backgroundImage: `url(${slide.image})` }"
        >
          <div class="slide-content">
            
            <p>{{ slide.feed }}</p>
            <p class="font-bold text-xl ">{{ slide.title }}</p>
          </div>
        </div>
      </div>
  
      <!-- Navigation Arrows -->
      <button class="prev-btn" @click="prevSlide">❮</button>
      <button class="next-btn" @click="nextSlide">❯</button>
  
      <!-- Pagination Dots -->
      <div class="dots">
        <span
          v-for="(slide, index) in slides"
          :key="index"
          class="dot"
          :class="{ active: index === currentIndex }"
          @click="goToSlide(index)"
        ></span>
      </div>
    </div>
      </center>
      <!-- <center>
        <p class="font-mono text-xl font-bold text-gray-700">-Lily Rose</p>
      </center> -->
    </div>

    <!-- Image Section -->
    <div class="block1 hidden md:flex h-[300px] w-[320px] md:ml-[80px] animate-on-scroll">
      <img
        src="https://themewagon.gitlab.io/restaurant/assets/img/food/pizza2.png"
        alt=""
        class="slide-in-left h-70 w-[300px]"
      />
    </div>
  </section>
</template>

<style scoped>
/* Initial state for animation */
.animate-on-scroll {
  opacity: 0;
  transform: translateX(50px);
  transition: opacity 0.8s ease-out 1s, transform 0.8s ease-out 1s;
}

/* Animated state */
.animate-on-scroll.animate {
  opacity: 1;
  transform: translateX(0);
}

.slide-in-left {
  transform: translateY(50px);
  opacity: 0;
  animation: slideInLeft 1s forwards;
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
  @media (max-width: 768px) {
    .feedback {
      margin-top: 380px;
    }
    #star{
      height: 20px;
    }
    img{
      display: none;
    }
  }

  


      .slider-container {
    position: relative;
    width: 100%;
    max-width: 800px;
    overflow: hidden;
    margin-top: -80px;
  }
  
  /* Slider Wrapper */
  .slider-wrapper {
    display: flex;
    transition: transform 0.5s ease-in-out;
  }
  
  /* Individual Slide */
  .slide {
    min-width: 100%;
    height: 400px;
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;
    justify-content: center;
    
    color: gray;
    
  }
  
  /* Slide Content */
  .slide-content {
    text-align: center;
  }
  
  /* Navigation Arrows */
  .prev-btn,
  .next-btn {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background: rgba(234, 159, 84, 0.139);
    color: white;
    border: none;
    padding: 10px;
    font-size: 20px;
    cursor: pointer;
    border-radius: 50%;
  }
  
  .prev-btn {
    left: 10px;
  }
  
  .next-btn {
    right: 10px;
  }
  
  .prev-btn:hover,
  .next-btn:hover {
    background: rgba(237, 144, 5, 0.877);
  }
  
  /* Pagination Dots */
  .dots {
    position: absolute;
    bottom: 20px;
    width: 100%;
    text-align: center;
  }
  
 
  
  .dot.active {
    background: white;
  }
</style>
