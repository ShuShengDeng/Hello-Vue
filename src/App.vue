<script setup lang="ts">
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Services from './components/Services.vue'
import Pets from './components/Pets.vue'
import About from './components/About.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="min-h-screen bg-white">
    <Header />
    <main>
      <Hero />
      <Services />
      <Pets />
      <About />
      <Contact />
    </main>
    <Footer />
  </div>
</template>
