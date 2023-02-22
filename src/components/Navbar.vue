<template>
  <header class="bg-white shadow h-16 flex justify-between items-stertch">
    <router-link :to="{ name: 'home' }" class="inline-flex items-center h-full px-5 text-orange-500 text-2xl"> Mealspedia </router-link>
    <div class="hidden md:block">
      <router-link :to="{ name: 'byName' }" class="inline-flex items-center px-2 h-full hover:bg-orange-500 hover:text-white transition-colors">
        Search Meals
      </router-link>
      <router-link :to="{ name: 'byLetter' }" class="inline-flex items-center px-2 h-full hover:bg-orange-500 hover:text-white transition-colors">
        Meals By Letter
      </router-link>
      <router-link :to="{ name: 'ingredients' }" class="inline-flex items-center px-2 h-full hover:bg-orange-500 hover:text-white transition-colors">
        Meals By Ingredients
      </router-link>
    </div>
    <div class="md:hidden flex items-center">
      <button @click="showMenu = !showMenu" class="inline-flex items-center justify-center h-full px-5">
        <svg v-if="!showMenu" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
        </svg>
        <svg v-else class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
        </svg>
      </button>
      <div v-show="showMenu" class="absolute top-16 right-0 left-0 bg-white shadow-md">
        <router-link :to="{ name: 'byName' }" class="block px-4 py-2 hover:bg-orange-500 hover:text-white transition-colors">
          Search Meals
        </router-link>
        <router-link :to="{ name: 'byLetter' }" class="block px-4 py-2 hover:bg-orange-500 hover:text-white transition-colors">
          Meals By Letter
        </router-link>
        <router-link :to="{ name: 'ingredients' }" class="block px-4 py-2 hover:bg-orange-500 hover:text-white transition-colors">
          Meals By Ingredients
        </router-link>
      </div>
    </div>
  </header>
</template>
<script setup>
import { ref } from "@vue/reactivity";

const showMenu = ref(false);
</script>
