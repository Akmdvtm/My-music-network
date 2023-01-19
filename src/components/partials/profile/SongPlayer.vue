<template>
  <div class="bg-green-500 rounded">
    <div id="aplayer"></div>
  </div>
</template>

<script setup>
import APlayer from 'aplayer'
import {onMounted} from "vue";
import 'aplayer/dist/APlayer.min.css'

onMounted(() => {
  thePlayer()
})

const thePlayer = () => {
  new APlayer({
    container: document.getElementById('aplayer'),
    audio: [{
      name: 'first',
      artist: 'artist',
      url: '/music/Travis Scott - HIGHEST IN THE ROOM (feat. Duke, Jones).mp3',
      cover: 'cover.jpg'
    }]
  });
}
</script>

<style scoped>

</style>