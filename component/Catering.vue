<template>
  <section>
    <!-- Heading Section -->
    <div class="text-center">
      <p class="head font-mono text-2xl pt-7 text-opacity-70">Catering</p>
      <h2 class="font-serif font-bold text-4xl mt-2">We Manage Your Events</h2>
      <p class="headp pl-5 pt-5 text-gray-500 text-sm font-mono font-medium leading-relaxed mt-5 text-base">
        Allow our Chef to deliver the perfect private dinner or cocktail party experience in your <br>home; or let us simply add a little extra flavor to your next office meeting, boat trip, or <br>beach picnic. By partnering with our sibling location Rosewater Wine & Spirits, we can <br>offer a full array of bar services and beverage selections. Email us to learn more.
      </p>
    </div>
    <br><br><br>

    <!-- Card Section -->
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
  @media screen and (max-width: 330px) {
    h2{
      font-size: 1.3rem;
    }
    .head{
      font-size: 1rem;
    }
  }
</style>