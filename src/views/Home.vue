<template>
  <!-- Hero Section -->
  <section
    class="relative bg-black text-white h-[100dvh] w-full flex flex-col justify-center items-center text-center px-4 overflow-hidden lg:grid lg:grid-cols-2 lg:place-items-center"
  >
    <div class="absolute lg:relative lg:pt-20 inset-0 z-0">
      <img
        :src="heroImage"
        class="w-full h-full object-cover scale-110 lg:scale-125"
        alt="Masked person holding a cake labeled Cake Heist"
      />
      <div class="absolute lg:w-[115%] lg:h-[110%] inset-0 bg-black opacity-40"></div>
    </div>
    <div class="z-10 pt-12 lg:px-20 md:pt-12 lg:text-left">
      <h1
        class="text-4xl md:text-5xl font-bold text-red-600 mb-4 drop-shadow-lg"
      >
        The Cake Heist Begins
      </h1>
      <p class="text-lg md:text-xl mb-6 text-gray-200">
        Dangerously delicious cakes, straight from the vault.
      </p>
      <router-link
        to="/"
        class="inline-block mt-4 lg:mt-0 text-lg px-6 py-3 border border-red-600 hover:text-red-600 bg-red-600 hover:bg-transparent text-black font-medium transition duration-300"
      >
        View The Loot
      </router-link>
    </div>
  </section>
  <div class="w-full h-px bg-gray-700"></div>
  <!-- Featured Products Section -->
  <section class="bg-[#111111] text-white py-20 px-6 md:px-10 lg:px-36">
    <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 text-[#e5e5e5]">
      This Week's Loot
    </h2>
    <div class="grid grid-cols-2 md:grid-cols-3 gap-6 max-w-6xl mx-auto">
      <div
        v-for="cake in cakes"
        :key="cake.id"
        class="overflow-hidden shadow-lg hover:shadow-red-700 transition transform hover:-translate-y-2 cursor-pointer"
      >
        <img
          :src="cake.image"
          :alt="cake.name"
          class="w-full h-32 md:h-40 lg:h-44 object-cover hover:opacity-100 transition"
        />
        <div class="p-2 pt-3">
          <h3 class="text-base text-gray-300 mb-1">{{ cake.name }}</h3>
          <p class="text-red-500 mb-2 text-[1.2rem]">{{ cake.price }}</p>
        </div>
      </div>
    </div>
    <div class="flex justify-center">
      <router-link
        to="cakes"
        class="mt-4 text-lg px-6 py-3 border border-red-600 text-red-600 hover:bg-red-600 hover:text-black font-medium transition duration-300"
      >
        Find More
      </router-link>
    </div>
  </section>
  <div class="w-full h-px bg-gray-700"></div>

  <section class="bg-[#111111] text-white py-20 px-6 md:px-10 lg:px-36">
    <div class="max-w-6xl mx-auto text-center">
      <h2
        class="text-3xl md:text-4xl font-bold text-center mb-12 text-[#e5e5e5]"
      >
        Explore Our Range
      </h2>
      <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-6">
        <div
          v-for="category in categories"
          :key="category.id"
          class="bg-[#1a1a1a] hover:bg-[#2a2a2a] border-l-4 border-red-600 rounded-lg p-6 flex flex-col justify-center items-start transition shadow-lg hover:shadow-red-700 text-left cursor-pointer"
        >
          <h3 class="text-lg font-bold text-red-500 mb-1">
            {{ category.name }}
          </h3>
          <p class="text-gray-400 text-sm">{{ category.description }}</p>
        </div>
      </div>
    </div>
  </section>
  <div class="w-full h-px bg-gray-700"></div>
  <!-- About  -->
  <section class="bg-[#111] text-white py-20 px-6 md:px-10 lg:px-36">
    <div class="max-w-4xl mx-auto text-center">
      <h2 class="text-3xl md:text-4xl font-bold text-red-600 mb-6">
        About the Heist
      </h2>
      <p class="text-gray-300 text-lg leading-relaxed text-pretty">
        At Cake Heist, we believe every dessert should feel like a steal.<br />
        Born from midnight cravings and sweet rebellion, we specialize in
        dangerously delicious cakes that defy the ordinary. Whether it's a
        birthday, a breakup, or just a Wednesday — our vault is always stocked
        and ready to be raided.
      </p>
      <router-link
        to="/about"
        class="inline-block mt-4 text-lg px-6 py-3 border border-red-600 text-red-600 hover:bg-red-600 hover:text-black font-medium transition duration-300"
      >
        About Us
      </router-link>
    </div>
  </section>
  <div class="w-full h-px bg-gray-700"></div>
  <!-- Follow us Section -->
  <section class="bg-[#060606] text-white py-20 px-6 md:px-10 lg:px-36">
    <div
      class="max-w-6xl mx-auto text-center flex flex-col justify-center items-center"
    >
      <h2 class="text-3xl md:text-4xl font-bold text-red-600 mb-6">
        Follow Us on Instagram
      </h2>
      <p class="text-gray-400 mb-6 text-lg">
        Catch behind-the-scenes, cake drops, and more.
      </p>
      <a
        href="https://instagram.com/cakeheist"
        target="_blank"
        class="flex items-center gap-1 w-fit mt-4 text-lg px-6 py-3 border border-red-600 text-red-600 hover:bg-red-600 hover:text-black font-medium transition duration-300"
      >
        <InstIcon />
        Cake Heist
      </a>
    </div>
  </section>
  <div class="w-full h-px bg-gray-700"></div>
</template>

<script setup>
import heroImage from "@/assets/images/guy_with_cake.png";
import InstIcon from "@/components/icons/instagram.vue";
const cakes = [
  {
    id: 1,
    name: "Vault Vanilla",
    price: "$15",
    image:
      "https://images.unsplash.com/photo-1606983340126-99ab4feaa64a?fm=jpg&q=60&w=3000&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8YmlydGhkYXklMjBjYWtlfGVufDB8fDB8fHww",
  },
  {
    id: 2,
    name: "Heist Chocolate",
    price: "$20",
    image:
      "data:image/jpeg;base64,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",
  },
  {
    id: 3,
    name: "Masked Red Velvet",
    price: "$18",
    image:
      "https://thecakeday.in/cdn/shop/products/82.png?v=1680192068&width=1445",
  },
  {
    id: 4,
    name: "Strawberry Swindle",
    price: "$17",
    image:
      "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqyG7A5aV6jNSg2J08R0wBEKGcCdNXgHHhSw&s",
  },
];

const categories = [
  {
    id: 1,
    name: "Cakes",
    description: "Signature full-size cakes in classic & creative flavors.",
  },
  {
    id: 2,
    name: "Cup Cakes",
    description: "Mini heists of flavor in every bite.",
  },
  { id: 3, name: "Brownies", description: "Dense, rich, and criminally good." },
  {
    id: 4,
    name: "Sundaes",
    description: "Layered desserts for your sweet escape.",
  },
  { id: 5, name: "Cookies", description: "Small loot, big flavor." },
  {
    id: 6,
    name: "Pies",
    description: "Filling-packed favorites from the vault.",
  },
];
</script>
