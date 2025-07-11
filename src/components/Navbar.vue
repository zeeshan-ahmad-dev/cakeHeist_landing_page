<template>
    <nav class="bg-[#070707] text-white p-4 z-50 fixed w-full flex justify-between items-center px-5 md:px-8">
        <div class="text-2xl font-bold tracking-wide">
           Cake<span class="bg-red-600 px-1 text-black">Heist</span>
        </div>
      <ul class="hidden md:flex space-x-4 text-sm md:text-base">
        <li><RouterLink to="/" class="hover:text-red-400">Home</RouterLink></li>
        <li><RouterLink to="/cakes" class="hover:text-red-400">Cakes</RouterLink></li>
        <li><RouterLink to="/about" class="hover:text-red-400">About</RouterLink></li>
        <li><RouterLink to="/order" class="hover:text-red-400">Order</RouterLink></li>
      </ul>
      <button @click="toggleMenu" class="md:hidden">
          <img :src="HamburgerIcon" class="size-8 z-[10000]" alt="">
      </button>

    </nav>
    <!-- Small screen sidebar links -->
     <div class="md:hidden bg-black text-white absolute z-[1000] flex flex-col items-center p-4 space-y-4 w-full transition-all duration-300" 
     :class="[mobileMenu ? 'top-16 opacity-100' : '-top-50 opacity-0 -z-50']">
          <RouterLink to="/home" class="block hover:text-red-400">Home</RouterLink>
          <RouterLink to="/cakes" class="block hover:text-red-400">Cakes</RouterLink>
          <RouterLink to="/about" class="block hover:text-red-400">About</RouterLink>
          <RouterLink to="/order" class="block hover:text-red-400">Order</RouterLink>
      </div>
  </template>

<script setup>
import { RouterLink } from 'vue-router';
import { ref } from 'vue';
import HamburgerIcon from '@/assets/icons/Hamburger.svg';

const mobileMenu = ref(false)
const toggleMenu = () => {
  mobileMenu.value = !mobileMenu.value
}
</script>
