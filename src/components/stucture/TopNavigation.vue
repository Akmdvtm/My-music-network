<template>
  <nav class="w-full px-4 bg-black relative z-20 text-white-200">
    <div class="container mx-auto max-w-4xl h-16 flex justify-between text-xs md:text-sm ">
      <div class="h-full flex items-center">
        <router-link class="flex justify-center items-center"
                     to="">
          <div class="text-white text-2xl"><b>MSN</b></div>
        </router-link>
      </div>
      <div class="h-full flex items-center">
        <FullScreenModal></FullScreenModal>
      </div>
    </div>
  </nav>
</template>
<script setup>
import FullScreenModal from "@/components/stucture/FullScreenModal.vue";
</script>