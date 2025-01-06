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
    { threshold: 0.5 } // Trigger when 25% of the element is visible
  );

  animatedElements.forEach((el) => observer.observe(el));
});
</script>

<template>
  <section>
      <div><center><p class="head font-mono text-3xl pt-7 animate-on-scroll " style="margin-top: 100px;">Menu</p></center></div>
      <div><center><h2 class="font-serif font-bold text-4xl animate-on-scroll">Taste Our Foods & Enjoy</h2></center></div>
      <div class="flex flex-wrap justify-between items-center mx-[20px] mt-[30px]">
          <div class="w-full sm:w-1/2 md:w-1/4 p-2">
              <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/bowl-delicious-dinner.png" alt="food" height="280" width="270" class="rounded-md cursor-pointer">
          </div>
          <div class="w-full sm:w-1/2 md:w-1/4 p-2">
              <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/sec.jpg" alt="food" height="280" width="270" class="rounded-md cursor-pointer">
          </div>
          <div class="w-full sm:w-1/2 md:w-1/4 p-2">
              <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/antioxidant-beverage-carrot-juice.png" alt="food" height="280" width="270" class="rounded-md cursor-pointer">
          </div>
          <div class="w-full sm:w-1/2 md:w-1/4 p-2">
              <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/bowl-calcium-cereal.png" alt="food" height="280" width="270" class="rounded-md cursor-pointer">
          </div>
      </div>
  </section>
</template>
<style scoped>

.animate-on-scroll {
  opacity: 0;
  transform: translateY(50px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}

/* Animated state */
.animate-on-scroll.animate {
  opacity: 1;
  transform: translateY(0);
}
  @media (max-width: 330px) {
    .head{
      font-size: 1rem;
    }
    h2{
      font-size: 1.3rem;
    }
  }
</style>