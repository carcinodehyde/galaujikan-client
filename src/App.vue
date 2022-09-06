<script setup>
import RadioClient from "./components/RadioClient.vue";
</script>

<template>
  <div id="app">
    <header class="header">
      <div class="container">
        <h1 class="site-title">Galau Jikan FM_</h1>
        <span class="site-tagline"></span>
      </div>
      <span aria-hidden class="header__glitch">Galau Jikan FM_</span>
      <span aria-hidden class="header__tag">EvL</span>
    </header>
    <main>
      <RadioClient />
    </main>
  </div>
</template>
