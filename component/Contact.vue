<template>
    <section class="h-[600px] w-full">
        
        <div class="w-full px-6 py-8 bg-white shadow-lg rounded-md bg-gray-100">
          <h1 class="text-3xl font-medium font-serif text-center mb-4 mt-[80px]">Feel free to drop us a line!</h1>
          <p class="text-sm text-center font-mono text-gray-600 mb-6">
            Let's talk if you have any query or suggestion. We are open to learn from you. <br>So don't hesitate to reach us anytime.
          </p>
          <form class="flex pt-[50px]">
            <div class="h-[300px] w-[630px]">
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
              <label for="copy" class="ml-2 font-serif text-md text-gray-700">Send me a copy</label>
            </div>
      
            </div>
            <div class="h-[300px] w-[630px]">
              <div class="mb-4 ml-4">
              <textarea
                id="message"
                class="w-full px-4 py-2 font-mono border border-gray-300 rounded-md focus:ring-2 focus:ring-yellow-300 focus:outline-none"
                placeholder="Type your message here"
                rows="4"
              ></textarea>
            </div>
            <button class="bg-gray-900 text-gray-100 ml-[20px] py-2 px-10 rounded-md cursor-pointer font-medium hover:bg-black font-sans text-opacity-70">
              GIVE US A SHOT</button>
          </div>
          </form>
        </div>
      
      
        </section>
</template>


