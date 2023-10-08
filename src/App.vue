<template>
  <div class="bg-gray-100 h-full">
    <header class="bg-white shadow-md h-16 flex justify-between items-strech">
      <router-link :to="{ name: 'home' }">Home </router-link>
      <div class="flex items-center gap-1">
        <router-link
          to="/"
          class="inline-flex items-center px2 h-full transition-colors hover:bg-purple-200"
          >Search Meals</router-link
        >
        <router-link
          to="/"
          class="inline-flex items-center px2 h-full transition-colors hover:bg-purple-200"
          >Meals By Letters</router-link
        >
        <router-link
          to="/"
          class="inline-flex items-center px2 h-full transition-colors hover:bg-purple-200"
          >Meals Ingredients</router-link
        >
      </div>
    </header>
    <main>
      <router-view />
    </main>
  </div>
</template>

<script setup></script>

<style scoped></style>
