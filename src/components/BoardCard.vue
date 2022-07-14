<script setup lang="ts">
import type { Board } from "@/types";
defineProps<{
  board: Board;
}>();
const randomColor = "#" + Math.floor(Math.random() * 16777215).toString(16);
</script>
<template>
  <router-link :to="`/boards/${board.id}`" class="block w-96">
    <div class="card" >
        <img :src="board.image?.downloadUrl" class="card-img-top" alt="...">
        <div class="card-body">
            <p class="card-text">{{board.title}}</p>
        </div>
    </div>
  </router-link>
</template>