<template>
  <div class="p-8">
    <div
      v-for="ingredient of ingredients"
      :key="ingredient.id"
      class="bg-white rounded p-3 mb-3 shadow"
    >
      <h3 class="text-2xl font-bold">{{ ingredient.strIngredient }}</h3>
      <p>{{ ingredient.strDescription }}</p>
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from "vue";
import axiosClient from "../axiosClient";

const ingredients = ref([]);

onMounted(() => {
  axiosClient.get("list.php?i=list").then(({ data }) => {
    debugger;
    ingredients.value = data.meals;
  });
});
</script>
