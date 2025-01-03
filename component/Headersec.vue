<template>
  <section
    class="w-full mt-[68px] flex flex-col md:flex-row justify-center items-center md:items-start"
    style="background: linear-gradient(to bottom, rgba(255, 255, 0, 0.5), rgba(255, 255, 0, 0));"
  >
  <aside class="leftaside mt-[80px] md:mt-0 md:ml-10">
      <img class="image"
        src="https://themewagon.gitlab.io/restaurant/assets/img/food/plate.png"
        alt="img"
      />
    </aside>
    <!-- Text Section -->
    <aside class="rightaside md:mt-0 mt-10 md:ml-0 text-center md:text-left">
      <div class="pt-10 md:pt-56 text-2xl md:text-4xl font-serif">
        <span>The Spectacle <strong>Before Us<br />Was Indeed</strong> Sublime.</span>
      </div>
      <div class="pt-5 text-gray-500 text-sm font-mono leading-relaxed hidden md:block">
        <p>
          Apparently, we had reached a great height in the atmosphere, <br />for
          the sky was a dead black, and which lifts the horizon of<br />the sea
          to the level of the spectator on a hillside.
        </p>
      </div>
      <div class="mt-10 flex flex-col md:flex-row md:justify-start space-y-5 md:space-y-0 md:space-x-10">
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

    <!-- Image Section -->
    <!-- <aside class="leftaside mt-[80px] md:mt-0 md:ml-10">
      <img
        src="https://themewagon.gitlab.io/restaurant/assets/img/food/plate.png"
        alt="img"
        class="w-[250px] h-[250px] md:w-[335px] md:h-[335px]"
      />
    </aside> -->
  </section>
</template>
<style scoped>
  .leftaside {
    display: flex;
  flex-direction: row;
  width: 20rem;
  }
  .image
  {
    margin-top: 8rem;
    transform: translateX(-130px); 
    display: flex;
    
  }
  @media screen and (max-width: 768px) {
    .image{
      transform: translateX(2px); 
    }
    section{
      margin-top: -5rem;
    }
  }
</style>