<template>
  <div class="">
    <h4 class="section-title">Troba el pastís ideal per a cada ocasió</h4>
    <div class="flex justify-center align-middle items-center">
      <div
        class="w-full grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 auto-cols-auto gap-4"
      >
        <categoryCard
          v-for="category in categoryList"
          :key="category.id"
          :cake="category"
          :title="category.title"
          :imageSrc="category.img"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import { useCakeStore } from "@/stores/cakeStore";
const cakeStore = useCakeStore();
const categoryList = cakeStore.categoryList;
</script>

<style></style>
