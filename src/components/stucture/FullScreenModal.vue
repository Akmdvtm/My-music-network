<template>
  <div>
    <button class="
      bg-transparent
      hover:bg-green-400
      text-white
      font-semibold
      hover:text-white
      py-1
      px-2
      hover:border-transparent
      rounded
    "
            @click="open = !open"
    >
      <i class="fa-solid fa-bars fa-xl"></i>
    </button>
    <div class="
      animated
      slideInDow
      faster
      fixed
      w-full
      h-full
      top-0
      left-0
      flex
      justify-center
      backdrop-blur-sm
    "
         v-if="open"
    >
      <div class="bg-black absolute w-full h-full opacity-75"></div>
      <div class="my-auto fixed border-white w-80 pt-16">
        <p class="text-2xl text-center text-white font-bold">Menu</p>
        <RouterLinkButton
            class="w-full text-center text-white text-lg mt-4"
            btnText="Profile"
            color="green"
            url="/account/profile"
            @click="open = !open"
        ></RouterLinkButton>
        <RouterLinkButton
            class="w-full text-center text-white text-lg mt-4"
            btnText="Close"
            color="red"
            @click="open = !open"
        ></RouterLinkButton>
      </div>
    </div>
  </div>
</template>

<script setup>
import {ref} from "vue";
import RouterLinkButton from "@/components/global/RouterLinkButton.vue";


const open = ref(false)
</script>