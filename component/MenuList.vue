<script setup>
    import { ref, onMounted } from 'vue';
    const currentTab=ref(0)
    const tabs=ref([
          { title: 'Breakfast' },
          { title: 'Lunch'},
          { title: 'Dinner' },
          { title: 'Desserts' },
          {title : 'Drinks'}
    ])
    
    function  selectTab(index){
      this.currentTab=index
      
    }

    onMounted(() => {
  const animatedSections = document.querySelectorAll(".animate-on-scroll");

  const observer = new IntersectionObserver(
    (entries, observer) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("animate");
          observer.unobserve(entry.target); // Trigger animation once
        }
      });
    },
    { threshold: 0.5 } // Trigger when 50% of the element is visible
  );

  animatedSections.forEach((section) => observer.observe(section));
});
</script>


<template>
    <section>
          <div class="mx-auto px-0">
          <div class="border-b-2 border-gray-300 mb-15">
          <div id="tab" class="flex space-x-2 justify-center">
          
          <button
            v-for="(tab, index) in tabs"
            :key="index"
            class="py-2 px-2 text-sm font-mono font-bold text-gray-600 hover:text-black focus:outline-none"
            :class="[
              'transition-colors duration-300 ease-in-out',
              currentTab === index ? 'border-b-2 border-yellow-400' : 'text-gray-500'
            ]"
            @click="selectTab(index)"
          >
            {{ tab.title }}
          </button>
        </div>
      </div>
      <br>
      <div class="block1 bg-gray-50 rounded-lg shadow-md flex justify-between p-4 py-8 px-10 mx-10 " style="background-image: url('https://themewagon.gitlab.io/restaurant/assets/img/food/egg.png'),url('https://themewagon.gitlab.io/restaurant/assets/img/food/bread.png'); background-repeat: no-repeat,no-repeat; background-position: top right,bottom left; background-size: 250px 250px,400px 100px;">
  
        <div v-for="(tab, index) in tabs" :key="index" v-show="currentTab === index">
          <div class="text-sm flex justify-between items-center ml-[30px] mt-[20px] space-y-2 flex-col lg:flex-row animate-on-scroll" onclick="showPopup()">
            <!-- <span>
           <img class="position-absolute r-0 t-0 ml-[300px]" src="https://themewagon.gitlab.io/restaurant/assets/img/food/egg.png" alt="omlet" height="300" width="200"> 
             </span> -->
             
      
            <div class="slide-in-bottom p-4 bg-transparent border-r-2 border-gray-300 h-150">
              <a class="text-decoration-none " href="#">
                <div class="flex justify-between flex-wrap">
  
                  <h2 class="font-bold text-black text-xl font-mono">BREAKFAST BOWL</h2>
                  <p class="font-bold text-red-600 text-opacity-70">$8.50</p>
                </div>
                <p class="font-mono text-sm text-gray-500">"Black Bean Cake, Greens, Tomato & Avocado Pico drizzled with Lime Cream (Add egg $1)"</p>
              </a>
              <br><br><br>
              <a class="text-decoration-none " href="#">
                <div class="flex justify-between">
                  <h2 class="font-bold text-black text-xl font-mono">EGG SANDWICH</h2>
                  <p class="font-bold text-red-600 text-opacity-70">$7.50</p>
                </div>
                <p class="font-mono text-sm text-gray-500">Everything Bagel with Cream Cheese, Bacon, Tomato, Red Onion, Basil Pesto, Arugula</p>
              </a>
              <br><br><br>
              <a class="text-decoration-none " href="#">
                <div class="flex justify-between">
                  <h2 class="font-bold text-black text-xl font-mono">BREAKFAST BURRITO</h2>
                  <p class="font-bold text-red-600 text-opacity-70">$9.50</p>
                </div>
                <p class="font-mono text-sm text-gray-500">Three Scrambled Eggs, Cheddar, our Housemade Black Bean Cake, Avocado, Pico, & Lime Cream</p>
              </a>
              <br><br><br><br><br><br>
            </div>
            <div class="slide-in-bottom p-4 bg-transparent border-r-2 border-gray-300 h-150 ml-4">
              <a class="text-decoration-none " href="#">
                <div class="flex justify-between">
                  <h2 class="font-bold text-black text-xl font-mono">VEGGIE JAMMIE</h2>
                  <p class="font-bold text-red-600 text-opacity-70">$5.50</p>
                </div>
                <p class="font-mono text-sm text-gray-500">Everything Bagel with our Homemade Tofu Herb Spread, Cucumber Tomato, Red Onion, & Arugula</p>
              </a>
              <br><br><br>
              <a class="text-decoration-none " href="#">
                <div class="flex justify-between">
                  <h2 class="font-bold text-black text-xl font-mono">SMOKED SALMON BAGEL</h2>
                  <p class="font-bold text-red-600 text-opacity-70">$9.50</p>
                </div>
                <p class="font-mono text-sm text-gray-500">Crushed Avocado topped with MV Sea Salt on Toasted Multigrain</p>
              </a>
              <br><br><br>
              <a class="text-decoration-none " href="#">
                <div class="flex justify-between">
                  <h2 class="font-bold text-black text-xl font-mono">BREAKFAST PASTRIES</h2>
                  <p class="font-bold text-red-600 text-opacity-70">$9.00</p>
                </div>
                <p class="font-mono text-sm text-gray-500">Three Scrambled Eggs, Cheddar, our Housemade Black Bean Cake, Avocado, Pico, & Lime Cream</p>
              </a>
              <br><br><br>
              <a class="text-decoration-none " href="#">
                <div class="flex justify-between">
                  <h2 class="font-bold text-black text-xl font-mono">FRIED EGG</h2>
                  <p class="font-bold text-red-600 text-opacity-70">$8.00</p>
                </div>
                <p class="font-mono text-sm text-gray-500">Three Fried Eggs, house hot sauce, local cheddar mac, lettuce, pickle & onion on a sesame roll</p>
              </a>
            </div>
            <div class="slide-in-bottom p-4 bg-transparent h-150">
              <a class="text-decoration-none " href="#">
                <div class="flex justify-between">
                  <h2 class="font-bold text-black text-xl font-mono">BREAKFAST JAMMIE</h2>
                  <p class="font-bold text-red-600 text-opacity-70">$6.50</p>
                </div>
                <p class="font-mono text-sm text-gray-500">Everything Bagel with Cream Cheese, Bacon, Tomato, Red Onion, Basil Pesto, Arugula</p>
              </a>
              <br><br><br>
              <a class="text-decoration-none " href="#">
                <div class="flex justify-between">
                  <h2 class="font-bold text-black text-xl font-mono">BAGEL WITH CREAM CHEESE</h2>
                  <p class="font-bold text-red-600 text-opacity-70">$6.00</p>
                </div>
                <p class="font-mono text-sm text-gray-500">Crushed Avocado topped with MV Sea Salt on Toasted Multigrain</p>
              </a>
              <br><br><br>
              <a class="text-decoration-none " href="#">
                <div class="flex justify-between">
                  <h2 class="font-bold text-black text-xl font-mono">AVOCADO TOAST</h2>
                  <p class="font-bold text-red-600 text-opacity-70">$7.50</p>
                </div>
                <p class="font-mono text-sm text-gray-500">Crushed Avocado topped with MV Sea Salt on Toasted Multigrain</p>
              </a>
              <br><br><br>
              <a class="text-decoration-none " href="#">
                <div class="flex justify-between">
                  <h2 class="font-bold text-black text-xl font-mono">AVOCADO TOAST</h2>
                  <p class="font-bold text-red-600 text-opacity-70">$6.50</p>
                </div>
                <p class="font-mono text-sm text-gray-500">Crushed Avocado topped with MV Sea Salt on Toasted Multigrain</p>
              </a>
            </div>
          </div>
        </div>
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

/* Animation Triggered State */
.animate-on-scroll.animate {
  opacity: 1;
  transform: translateY(0);
}

 @media (max-width: 450px) {
  #tab {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 0px;
  }

  #tab button {
    font-size: 0.5rem; /* Decrease font size */
    padding: 0.5rem 0rem; /* Decrease padding */
  }
}
/* 

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
} */

</style>
