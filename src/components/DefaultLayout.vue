<template>
  <div class="bg-gray-100 h-full">
    <Navbar />
    <main>
      <router-view class="max-w-[1200px] mx-auto" />
    </main>
  </div>
</template>

<script setup>
import Navbar from "../components/Navbar.vue";
</script>
