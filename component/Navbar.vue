<template>
  <nav
    class="navbar fixed top-0 left-0 right-0 w-full z-50 bg-black text-white flex justify-between items-center p-2"
  >
    <!-- Logo -->
    <div class="logo ml-4 md:ml-14">
      <img
        src="https://themewagon.gitlab.io/restaurant/assets/img/logo.png"
        alt="logo"
        class="h-8"
      />
    </div>

    <!-- Hamburger menu -->
    <div class="lg:hidden">
      <button
        id="hamburger"
        class="text-white focus:outline-none"
        onclick="document.getElementById('menu').classList.toggle('hidden')"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16m-7 6h7"
          />
        </svg>
      </button>
    </div>

    <!-- Navigation Links -->
    <div
      id="menu"
      class="hidden lg:flex flex-col md:flex-row md:items-center md:space-x-8 w-full md:w-auto bg-black md:bg-transparent p-4 md:p-0"
    >
      <ul
        class="nav-links flex flex-col md:flex-row lg:space-x-6 md:space-y-0 md:space-x-8"
      >
        <li class="relative group text-gray-400 transition-colors cursor-pointer hover:text-white">
          Home
          <div
            class="absolute left-0 hidden pt-2 group-hover:block"
          >
            <div class="w-48 bg-black shadow-lg py-2">
              <a
                href="#"
                class="block px-4 py-2 text-gray-400 hover:text-white font-mono text-sm"
                >Header Static</a
              >
              <a
                href="#"
                class="block px-4 py-2 text-gray-400 hover:text-white font-mono text-sm"
                >Header Slider</a
              >
              <a
                href="#"
                class="block px-4 py-2 text-gray-400 hover:text-white font-mono text-sm"
                >Youtube Background</a
              >
              <a
                href="#"
                class="block px-4 py-2 text-gray-400 hover:text-white font-mono text-sm"
                >Self Hosted Video</a
              >
              <a
                href="#"
                class="block px-4 py-2 text-gray-400 hover:text-white font-mono text-sm"
                >RTL</a
              >
            </div>
          </div>
        </li>
        <li class="text-gray-400 transition-colors cursor-pointer hover:text-white">
          Pages
        </li>
        <li class="text-gray-400 transition-colors cursor-pointer hover:text-white">
          Menu
        </li>
        <li class="text-gray-400 transition-colors cursor-pointer hover:text-white">
          Components
        </li>
        <li class="text-gray-400 transition-colors cursor-pointer hover:text-white">
          Utilities
        </li>
        <li class="text-gray-400 transition-colors cursor-pointer hover:text-white">
          Plugins
        </li>
      </ul>

      <!-- Reservation Button -->
      <button
        id="btn"
        class="mt-4 md:mt-0 text-yellow-400 border-2 border-yellow-400 bg-transparent px-12 py-3 rounded-md cursor-pointer hover:bg-yellow-400 hover:text-white"
      >
        MAKE A RESERVATION
      </button>
    </div>
  </nav>

  
</template>

