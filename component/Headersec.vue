<template>
  <section
    class="w-full mt-[68px] flex flex-col md:flex-row justify-center items-center md:items-start"
    style="background-image: url('https://themewagon.gitlab.io/restaurant/assets/img/food/Vector.png'); background-repeat: no-repeat; background-size: 35%; background-position: left;"
  >
    <!-- Rotating Image Section -->
    <aside class="leftaside mt-[80px] md:mt-0 lg:ml-10">
      <img
        class="image rotate-on-scroll"
        src="https://themewagon.gitlab.io/restaurant/assets/img/food/plate.png"
        alt="Rotating Plate"
      />
    </aside>

    <!-- Text Section -->
    <aside class="rightaside md:mt-0 mt-10 md:ml-0 text-center md:text-left">
      <div class="text-slide-in slide-in-bottom pt-10 md:pt-56 text-2xl md:text-4xl font-serif">
        <span>The Spectacle <strong>Before Us<br />Was Indeed</strong> Sublime.</span>
      </div>
      <div
        class="text-slide-in slide-in-bottom2 pt-5 text-gray-500 text-sm font-mono leading-relaxed hidden md:block"
      >
        <p>
          Apparently, we had reached a great height in the atmosphere, <br />
          for the sky was a dead black, and which lifts the horizon of<br />the
          sea to the level of the spectator on a hillside.
        </p>
      </div>
      <div
        class="button-slide-in mt-10 flex flex-col md:flex-row md:justify-start space-y-5 md:space-y-0 md:space-x-10"
      >
        <button
          class="bg-yellow-400 text-gray-800 py-3 px-10 rounded-md cursor-pointer hover:bg-yellow-500 font-sans"
        >
          <b>ORDER ONLINE</b>
        </button>
        <button
          class="border-2 border-yellow-400 text-yellow-400 py-3 px-10 rounded-md cursor-pointer hover:bg-yellow-400 hover:text-gray-800 font-sans"
        >
          <b>OUR LOCATION</b>
        </button>
      </div>
    </aside>
  </section>
</template>

<script setup>
import { onMounted } from "vue";

onMounted(() => {
  const rotatingImages = document.querySelectorAll(".rotate-on-scroll");
  const animatedElements = document.querySelectorAll(".text-slide-in, .button-slide-in");

  const observer = new IntersectionObserver(
    (entries, observer) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("animate");
          observer.unobserve(entry.target); // Unobserve after triggering
        }
      });
    },
    { threshold: 0.5 } // Trigger when 50% of the element is visible
  );

  rotatingImages.forEach((img) => observer.observe(img));
  animatedElements.forEach((el) => observer.observe(el));
});
</script>

<style scoped>
/* Rotating image animation */
.rotate-on-scroll {
  transform: translate(-300px, -0px) rotate(-90deg); /* Start from top-left corner */
  transition: transform 1.5s ease-out; /* Smooth animation */
}
.rotate-on-scroll.animate {
  transform: translate(0, 0) rotate(0deg); /* Final position and rotation */
}

/* Text fade-in and slide-in animation */
.text-slide-in {
  opacity: 0;
  transform: translateY(50px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}
.text-slide-in.animate {
  opacity: 1;
  transform: translateY(0);
}

/* Button fade-in and slide-in animation */
.button-slide-in {
  opacity: 0;
  transform: translateY(50px);
  transition: opacity 1s ease-out, transform 1s ease-out;
}
.button-slide-in.animate {
  opacity: 1;
  transform: translateY(0);
}

/* Styling for responsiveness */
.leftaside {
  display: flex;
  flex-direction: row;
  width: 20rem;
}
.image {
  margin-top: 8rem;
  width: 300px;
  height: 300px;
  position: relative;
}

/* Mobile adjustments */
@media screen and (max-width: 768px) {
  .image {
    transform: none;
    margin-top: 4rem;
  }
  section {
    margin-top: -2rem;
  }
}
</style>
