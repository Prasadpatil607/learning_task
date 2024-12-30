<template>
  <div>
    <nav class="navbar fixed-top fixed top-0 left-0 w-full z-50 bg-black text-white flex justify-between items-center p-2">
      <div class="logo ml-14">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/logo.png" alt="logo">
      </div>
      <ul class="nav-links flex space-x-8 mr-80">
        <li><a href="#" class="text-white text-opacity-70">Home</a></li>
        <li><a href="#" class="text-white text-opacity-70">Pages</a></li>
        <li><a href="#" class="text-white text-opacity-70">Menu</a></li>
        <li><a href="#" class="text-white text-opacity-70">Components</a></li>
        <li><a href="#" class="text-white text-opacity-70">Utilities</a></li>
        <li><a href="#" class="text-white text-opacity-70">Plugins</a></li>
      </ul>
      <button id="btn" class="ml-[-200px] text-yellow-400 border-2 border-yellow-400 bg-transparent px-12 py-3 rounded-md cursor-pointer hover:bg-yellow-400 hover:text-white">
        <p>MAKE A RESERVATION</p>
      </button>
    </nav>
    <section class="home">
      <aside class="leftaside relative mt-[130px] ml-[10%] ml-[80px]">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/plate.png" alt="img" height="335" width="335">
      </aside>
      <aside class="rightaside relative md:text-left mt-[-490px] lg:ml-[480px]">
        <div class="heading1 pt-56 pl-5 text-4xl font-serif">
          <span>The Spectacle <strong>Before Us<br>Was Indeed</strong> Sublime.</span>
        </div>
        <div class="headp pl-5 pt-5 text-gray-500 text-sm font-mono leading-relaxed">
          <p>Apparently, we had reached a great height in the atmosphere, <br>for the sky was a dead black, and which lifts the horizon of<br>the sea to the level of the spectator on a hillside.</p>
        </div>
        <div class="hbtns mt-10 flex md:justify-start space-x-10">
          <button id="btn1" class="bg-yellow-400 text-gray-800 py-3 px-10 rounded-md cursor-pointer hover:bg-yellow-500 font-sans">
            <b>ORDER ONLINE</b>
          </button>
          <button id="btn2" class="border-2 border-yellow-400 text-yellow-400 py-3 px-10 rounded-md cursor-pointer hover:bg-yellow-400 hover:text-gray-800 font-sans">
            <b>OUR LOCATION</b>
          </button>
        </div>
      </aside>
    </section>
    <section>
      <div><center><p class="font-mono text-3xl pt-7" style="margin-top: 100px;">Menu</p></center></div>
      <div><center><h2 class="font-serif font-bold text-4xl">Taste Our Foods & Enjoy</h2></center></div>
      <div class="flex justify-between items-center ml-[80px] mr-[80px] mt-[30px]">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/bowl-delicious-dinner.png" alt="food" height="280" width="270" class="rounded-md cursor-pointer">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/sec.jpg" alt="food" height="280" width="270" class="rounded-md cursor-pointer">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/antioxidant-beverage-carrot-juice.png" alt="food" height="280" width="270" class="rounded-md cursor-pointer">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/bowl-calcium-cereal.png" alt="food" height="280" width="270" class="rounded-md cursor-pointer">
      </div>
    </section>
    <br><br><br>
    <section>
        <div class="w-[1100px] mx-auto px-0">
        <div class="border-b-2 border-gray-300 mb-15">
        <div class="flex space-x-4">
    
        <button
          v-for="(tab, index) in tabs"
          :key="index"
          class="py-2 px-6 ml-[280px] text-base font-medium text-gray-600 hover:text-black focus:outline-none"
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
    <div class="bg-gray-50 rounded-lg shadow-md flex justify-between p-4">
      <div v-for="(tab, index) in tabs" :key="index" v-show="currentTab === index">
        <div class="text-sm flex justify-between items-center ml-[30px] mr-[30px] mt-[20px] space-y-2 p-4">
          <!-- <span>
         <img class="position-absolute r-0 t-0 ml-[300px]" src="https://themewagon.gitlab.io/restaurant/assets/img/food/egg.png" alt="omlet" height="300" width="200"> 
           </span> -->
          <div class="p-4 bg-gray-50 border-r-2 border-gray-300 w-[320px] h-150">
            <a class="text-decoration-none " href="#">
              <div class="flex justify-between">
                
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
            <br><br><br>
            <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/bread.png" alt="" class="relative r-0 b-0 w-[300px] h-30">
          </div>
          <div class="p-4 bg-gray-50 border-r-2 border-gray-300 w-[320px] h-150 ml-4">
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
          <div class="p-4 bg-gray-50 w-[320px] h-150">
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
  <br><br><br><br><br><br>
    <section class="bg-black w-full h-65 flex justify-center items-center">
      <div class="h-80 w-90 ">
        <img class="mt-[-90px]" src="https://themewagon.gitlab.io/restaurant/assets/img/food/fried-clipart-transparent-background-7.png" alt="img" height="350" width="350">
      </div>
      <div class="bg-yellow h-30 w-80 ml-[30px] mt-[40px]">
        <p class="text-yellow-400 font-bold text-md font-mono">Hungry?</p>
        <h1 class="text-white font-serif font-bold text-xl">We will home deliver!</h1><br>
        <button class="bg-yellow-400 text-gray-800 py-2 px-10 rounded-md cursor-pointer hover:bg-yellow-500 font-sans font-medium text-opacity-70">
            MAKE AN ORDER
          </button>
      </div>
    </section>
    <br><br>
    <section>
      <div><center><p class="font-mono text-2xl pt-7 text-opacity-70" >Catering</p></center></div>
      <div><center><h2 class="font-serif font-bold text-4xl">We Manage Your Events</h2>
        <p class="headp pl-5 pt-5 text-gray-500 text-sm font-mono font-medium leading-relaxed mt-5 text-base">Allow our Chef to deliver the perfect private dinner or cocktail party experience in your <br>home; or let us simply add a little extra flavor to your next office meeting, boat trip, or <br>beach picnic. By partnering with our sibling location Rosewater Wine & Spirits, we can <br>offer a full array of bar services and beverage selections. Email us to learn more.</p>
      </center></div>
        <br><br><br>
      <center><div class="w-[600px] h-60 rounded-md shadow-lg flex justify-center items-center hover:shadow-xl transition-all duration-300">
        <div class="h-60 w-60">
          <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/pancake_PNG94.png" alt="">
        </div>
        <div class="h-60 w-60 mt-[85px]">
          <p class="font-bold text-opacity-70">We Cater in Weddings,<br>Corporate Functions <br>and Events</p><br>
          <button class="bg-yellow-400 text-gray-800 py-2 px-10 rounded-md cursor-pointer hover:bg-yellow-500 font-sans text-opacity-70">
            HIRE US NOW
          </button>
        </div>
      </div></center>
    </section>
    <br><br><br>

    <section class="h-[500px]">
      
      <div class="grid grid-cols-4 gap-2 p-4 pl-20 rounded h-[450px] justify-between items-center">
    
    <div class="bg-white bg-opacity-80 rounded col-span-1 row-span-2 h-[420px] w-[400px]">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/bigimg.jpg" class="rounded h-[420px] w-[400px] cursor-pointer hover:shadow-2xl transition-all duration-400" alt="img1">
    </div>
    <div class="bg-white bg-opacity-80 text-center text-2xl h-[200px] w-[200px] flex items-center justify-center ml-[130px]">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/1.jpg" alt="img2" class="rounded cursor-pointer hover:shadow-2xl transition-all duration-400">
    </div>
    <div class="bg-white bg-opacity-80 text-center text-2xl h-[200px] w-[200px] flex items-center justify-center ml-[70px]">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/2.jpg" alt="img3" class="rounded cursor-pointer hover:shadow-2xl transition-all duration-400">
    </div>
    <div class="bg-white bg-opacity-80 text-center text-2xl h-[200px] w-[200px] flex items-center justify-center">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/3.jpg" alt="img4" class="rounded cursor-pointer hover:shadow-2xl transition-all duration-400">
    </div>
    <div class="bg-white bg-opacity-80 text-center text-2xl h-[200px] w-[200px] flex items-center justify-center ml-[130px]">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/4.jpg" alt="img5" class="rounded cursor-pointer hover:shadow-2xl transition-all duration-400">
    </div>
    <div class="bg-white bg-opacity-80 text-center text-2xl h-[200px] w-[200px] flex items-center justify-center ml-[70px]">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/5.jpg" alt="img6" class="rounded cursor-pointer hover:shadow-2xl transition-all duration-400">
    </div>
    <div class="bg-white bg-opacity-80 text-center text-2xl h-[200px] w-[200px] flex items-center justify-center">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/gallery/thumb/6.jpg" alt="img7" class="rounded cursor-pointer hover:shadow-2xl transition-all duration-400">
    </div>
</div>

    </section>
      <br><br><br>
    <section class="ml-[80px]">
      <div><p class="font-mono text-2xl pt-7 text-opacity-70" >About Us</p></div>
      <div><h2 class="font-serif font-bold text-3xl">Who Are We?</h2>
        <p class=" pt-5 text-gray-500 text-sm font-mono font-medium leading-relaxed text-base">We are a chain of theme restaurant founded in 1971 in London. In <br>1979, the cafe began covering its walls with rock and roll <br>memorabilia, a tradition which expanded to others in the chain.</p>
      </div>
      <br>
      <button class="bg-yellow-400 text-gray-800 py-2 px-10 rounded-md cursor-pointer font-bold hover:bg-yellow-500 font-sans text-opacity-70">
            LEARN MORE
          </button>
        <div class="h-[500px] w-[600px]">
          <div class="grid grid-cols-3 gap-4 p-2 py-4 mt-8">
    
            <div class="h-[170px] w-[170px]">
              <img src="https://themewagon.gitlab.io/restaurant/assets/img/team/1.png" alt="" class="rounded-lg" style="border-radius: 50%;">
              <p class="text-white-400 font-bold text-md font-mono px-4">Gordon Ramsey</p>
              <p class="text-white-50 font-mono text-md text-opacity-80 px-4 text-sm">Owner & Founder</p>
            </div>
            <div class=" h-[170px] w-[170px] col-start-3 row-start-1">
              <img src="https://themewagon.gitlab.io/restaurant/assets/img/team/2.png" alt="" class="rounded-lg" style="border-radius: 50%;">
              <p class="text-white-400 font-bold text-md font-mono px-4">Gordon Ramsey</p>
              <p class="text-white-50 font-mono text-md text-opacity-80 px-4 text-sm">Owner & Founder</p>
            </div>
            <div class=" h-[170px] w-[170px]">
              <img src="https://themewagon.gitlab.io/restaurant/assets/img/team/3.png" alt="" class="rounded-lg" style="border-radius: 50%;">
              <p class="text-white-400 font-bold text-md font-mono px-4">Gordon Ramsey</p>
              <p class="text-white-50 font-mono text-md text-opacity-80 px-4 text-sm">Owner & Founder</p>
            </div>
            <div class="h-[170px] w-[170px] mt-10">
              <img src="https://themewagon.gitlab.io/restaurant/assets/img/team/4.png" alt="" class="rounded-lg" style="border-radius: 50%;">
              <p class="text-white-400 font-bold text-md font-mono px-4">Gordon Ramsey</p>
              <p class="text-white-50 font-mono text-md text-opacity-80 px-4 text-sm">Owner & Founder</p>
            </div>
            <div class="h-[170px] w-[170px] mt-10">
              <img src="https://themewagon.gitlab.io/restaurant/assets/img/team/5.png" alt="" class="rounded-lg" style="border-radius: 50%;">
              <p class="text-white-400 font-bold text-md font-mono px-4">Gordon Ramsey</p>
              <p class="text-white-50 font-mono text-md text-opacity-80 px-4 text-sm">Owner & Founder</p>
            </div>
            <div class="h-[170px] w-[170px] mt-10">
              <img src="https://themewagon.gitlab.io/restaurant/assets/img/team/6.png" alt="" class="rounded-lg" style="border-radius: 50%;">
              <p class="text-white-400 font-bold text-md font-mono px-4">Gordon Ramsey</p>
              <p class="text-white-50 font-mono text-md text-opacity-80 px-4 text-sm">Owner & Founder</p>
            </div>
          </div>
        </div>

      <div class="h-80 w-[500px] ml-[685px] mt-[-600px]">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/food/soup.png" alt="soup">
      </div>
    </section>
    <section style="background-image: url('	https://themewagon.gitlab.io/restaurant/assets/img/food/green.png'); background-repeat: no-repeat; b"></section>
  </div>


</template>

<style scoped>
#btn{
  cursor: pointer;
}
#aside{
  height: 200px;
  width: 200px;
  background-color: aqua;
}
</style>
<script setup>
  import { ref } from 'vue';
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
</script>

