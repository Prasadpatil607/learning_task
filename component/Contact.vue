<template>
  <section class="h-auto w-full bg-gray-100">
    <div class="w-full px-4 py-6 md:px-6 md:py-8 bg-white shadow-lg rounded-md">
      <!-- Heading Section -->
      <h1 class="text-2xl md:text-3xl font-medium font-serif text-center mb-4 mt-12 md:mt-[80px]">
        Feel free to drop us a line!
      </h1>
      <p class="text-sm md:text-base text-center font-mono text-gray-600 mb-6">
        Let's talk if you have any query or suggestion. We are open to learn from you. <br>
        So don't hesitate to reach us anytime.
      </p>

      <!-- Form Section -->
      <form class="flex flex-col md:flex-row pt-6 md:pt-[50px] space-y-6 md:space-y-0 md:space-x-6">
        <!-- Left Column -->
        <div class="h-auto md:h-[300px] w-full md:w-[50%]">
          <div class="mb-4">
            <input
              type="text"
              id="name"
              class="w-full px-4 py-2 font-mono border border-gray-300 rounded-md focus:ring-2 focus:ring-yellow-300 focus:outline-none"
              placeholder="Your Name"
            />
          </div>
          <div class="mb-4">
            <input
              type="text"
              id="subject"
              class="w-full px-4 py-2 font-mono border border-gray-300 rounded-md focus:ring-2 focus:ring-yellow-300 focus:outline-none"
              placeholder="Subject"
            />
          </div>
          <div class="mb-4">
            <input
              type="email"
              id="email"
              class="w-full px-4 py-2 font-mono border border-gray-300 rounded-md focus:ring-2 focus:ring-yellow-300 focus:outline-none"
              placeholder="Email Address"
            />
          </div>
          <div class="mb-4 flex items-center">
            <input
              type="checkbox"
              id="copy"
              class="h-4 w-4 accent-yellow-400 border-gray-300 rounded focus:ring-yellow-300"
            />
            <label for="copy" class="ml-2 font-serif text-sm md:text-md text-gray-700">
              Send me a copy
            </label>
          </div>
        </div>

        <!-- Right Column -->
        <div class="h-auto md:h-[300px] w-full md:w-[50%]">
          <div class="mb-4">
            <textarea
              id="message"
              class="w-full px-4 py-2 font-mono border border-gray-300 rounded-md focus:ring-2 focus:ring-yellow-300 focus:outline-none"
              placeholder="Type your message here"
              rows="4"
            ></textarea>
          </div>
          <div class="flex justify-center md:justify-start">
            <button class="bg-gray-900 text-gray-100 py-2 px-6 md:px-10 rounded-md cursor-pointer font-medium hover:bg-black font-sans text-opacity-70">
              GIVE US A SHOT
            </button>
          </div>
        </div>
      </form>
    </div>
  </section>
</template>
