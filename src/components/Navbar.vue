<template>
  <header class="bg-white shadow h-16 flex justify-between items-stertch">
    <router-link :to="{ name: 'home' }" class="inline-flex items-center h-full px-5"> Home </router-link>
    <div>
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
  </header>
</template>
