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

</style>