<template>
    <section class="block1 error h-[420px] w-full bg-gray-300 ">
        <center>
          <div class=" pt-[140px]">
            <img src="https://maps.gstatic.com/mapfiles/api-3/images/icon_error.png" alt="">
          </div>
          <div class="pt-2">
            <h1 class="text-2xl font-sans">Oops! Something went wrong.</h1><br>
            <p class="text-sm font-sans">This page didn't load Google Maps correctly. See the JavaScript console for technical details.</p>
          </div>
        </center>
      </section>
</template>

<style scoped>
  @media (max-width: 768px) {
    .error {
      margin-top: 380px;
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
        animation: slideInBottom 2s forwards;
        animation-timeline: view();
        animation-range: entry 0% cover 50%;
      }
</style>

