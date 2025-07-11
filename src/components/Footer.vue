<template>
    <!-- Footer -->
    <footer class="bg-black text-gray-400 py-10 px-6">
      <div class="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-6 md:text-left">
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
  
        <!-- Contact Info -->
        <div>
          <h4 class="text-lg font-semibold text-white mb-2">Contact Us</h4>
          <p class="text-sm">
            Nowshera Mardan Rd, Irum Colony, Mardan, 23200<br />
            <a href="tel:+923105888923" class="text-red-500 hover:underline">
              0310 5888923
            </a><br />
            <a
              href="mailto:cakeheist03@gmail.com"
              class="text-red-500 hover:underline"
            >
              cakeheist03@gmail.com
            </a>
          </p>
        </div>
  
        <!-- Developer Info -->
        <div>
          <h4 class="text-lg font-semibold text-white mb-2">Built By</h4>
          <p class="text-sm">
            Zeeshan Ahmad - Full Stack Developer<br />
            <a
              href="https://github.com/zeeshan-ahmad-dev"
              target="_blank"
              class="text-red-500 hover:underline"
            >
              GitHub
            </a>
            |
            <a
              href="https://my-portfolio-z.netlify.app/"
              target="_blank"
              class="text-red-500 hover:underline"
            >
              Portfolio
            </a>
          </p>
        </div>
      </div>
  
      <!-- Bottom bar -->
      <div class="mt-10 border-t border-gray-800 pt-4 text-center text-xs text-gray-500">
        &copy; {{ new Date().getFullYear() }} CakeHeist. All rights reserved.
      </div>
    </footer>
  </template>
  