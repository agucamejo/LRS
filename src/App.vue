<script setup>
import Navbar from './components/Navbar.vue';
import Premios from './components/Premios.vue';
import Musica from './components/Musica.vue';
</script>

<template>
  <header>
    <Navbar />
  </header>
  <main>
    <div id="videoContainer">
      <video id="videoBackground" autoplay="" muted="" loop="">
        <source src="./assets/video/video-background.mp4">
      </video>
    </div>
    <Premios />
    <Musica />
  </main>
</template>

