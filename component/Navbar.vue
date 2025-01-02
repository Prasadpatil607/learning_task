<template>
    <nav class="navbar fixed-top fixed top-0 left-0 w-full z-50 bg-black text-white flex justify-between items-center p-2">
      <div class="logo ml-14">
        <img src="https://themewagon.gitlab.io/restaurant/assets/img/logo.png" alt="logo">
      </div>
      <div class="flex">
      <ul class="nav-links flex space-x-8 mr-80">
        <div class="flex items-center space-x-6">
        <div class="relative group">
          <li class="text-gray-400 transition-colors cursor-pointer hover:text-white">
            Home
          </li>
          <div class="absolute left-0 hidden pt-4 group-hover:block">
            <div class="w-48 bg-black shadow-lg py-2">
              <a href="#" class="block px-4 py-2 text-gray-400 hover:text-white font-mono text-sm"
                >Header Static</a>
              <a href="#" class="block px-4 py-2 text-gray-400 hover:text-white font-mono text-sm"
                >Header Slider</a>
              <a href="#" class="block px-4 py-2 text-gray-400 hover:text-white font-mono text-sm"
                >Youtube Background</a>
              <a href="#" class="block px-4 py-2 text-gray-400 hover:text-white font-mono text-sm"
                >Self Hosted Video</a>
              <a href="#" class="block px-4 py-2 text-gray-400 hover:text-white font-mono text-sm"
                >RTL</a>
            </div>
          </div>
        </div>
        </div>
        <div class="flex items-center space-x-6">
        <div class="relative group">
          <li class="text-gray-400 transition-colors cursor-pointer hover:text-white">
            Pages
          </li>
          <div class="absolute left-0 hidden pt-4 group-hover:block">
            <div class="w-48 bg-black shadow-lg py-2">
              <a href="#" class="block px-4 py-1 text-gray-400 hover:text-white font-mono text-sm"
                >Menu</a>
              <a href="#" class="block px-4 py-1 text-gray-400 hover:text-white font-mono text-sm"
                >Gallery</a>
              <a href="#" class="block px-4 py-1 text-gray-400 hover:text-white font-mono text-sm"
                >About</a>
              <a href="#" class="block px-4 py-1 text-gray-400 hover:text-white font-mono text-sm"
                >Contact</a>
            </div>
          </div>
        </div>
        </div>
        <div class="flex items-center space-x-6">
        <div class="relative group">
          <li class="text-gray-400 transition-colors cursor-pointer hover:text-white">
            Menu
          </li>
        </div>
        </div>
        <div class="flex items-center space-x-6">
        <div class="relative group">
          <li class="text-gray-400 transition-colors cursor-pointer hover:text-white">
            Components
          </li>
        </div>
        </div>
        <div class="flex items-center space-x-6">
        <div class="relative group">
          <li class="text-gray-400 transition-colors cursor-pointer hover:text-white">
            Utilities
          </li>
        </div>
        </div>
        <div class="flex items-center space-x-6">
        <div class="relative group">
          <li class="text-gray-400 transition-colors cursor-pointer hover:text-white">
            Plugins
          </li>
        </div>
        </div>
      </ul>
      <button id="btn" class="ml-[-200px] text-yellow-400 border-2 border-yellow-400 bg-transparent px-12 py-3 rounded-md cursor-pointer hover:bg-yellow-400 hover:text-white">
        <p>MAKE A RESERVATION</p>
      </button>
    </div>
    </nav>
</template>

