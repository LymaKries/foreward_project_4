<template>
  <div class="w-full h-full bg-zinc-800 border-4 border-zinc-500 rounded">
    <div class="h-full flex flex-col justify-evenly content-evenly">
      <Title />

      <div class="w-full flex flex-col items-center">
        <div class="w-80 h-14 mb-3 bg-white border-2 border-zinc-500 rounded bottom-80"></div>
        <div class="w-96 h-96 bg-zinc-700 mb-3 border-4 border-zinc-400 rounded"></div>
      </div>

      <BottomText />
    </div>
  </div>
</template>
<script setup>
import BottomText from "./BottomText.vue";
</script>
<script setup>
import Title from "./Title.vue";
</script>
