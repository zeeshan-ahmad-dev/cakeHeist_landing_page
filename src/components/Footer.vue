<template>
    
  <!-- Footer  -->
  <footer class="bg-black text-gray-400 py-10 px-6">
    <div
      class="max-w-6xl mx-auto grid grid-cols-2 gap-6 md:text-left"
    >
      <!-- Brand / Logo -->
      <div>
        <h3 class="text-2xl font-bold text-white mb-2">
          Cake<span class="text-red-500">Heist</span>
        </h3>
        <p class="text-sm text-gray-500">
          Dangerously delicious cakes<br />
          straight from the vault.
        </p>
      </div>


      <!-- Contact or Social -->
      <div>
        <h4 class="text-lg font-semibold text-white mb-2">Contact Us</h4>
        <p class="text-sm">
          Karachi, Pakistan<br />
          <a href="tel:+923195888923" class="text-red-500 hover:underline"
            >0319 5888923</a
          ><br />
          <a
            href="mailto:contact@cakeheist.com"
            class="text-red-500 hover:underline"
            >contact@cakeheist.com</a
          >
        </p>
      </div>
    </div>

    <!-- Bottom bar -->
    <div
      class="mt-10 border-t border-gray-800 pt-4 text-center text-xs text-gray-500"
    >
      &copy; {{ new Date().getFullYear() }} CakeHeist. All rights reserved.
    </div>
  </footer>
</template>