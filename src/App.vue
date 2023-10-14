<script setup lang="ts">
import NavBar from './components/NavBar.vue';
import HomeComponent from './components/HomeComponent.vue';
import AboutComponent from './components/AboutComponent.vue';
import ProjectComponent from './components/ProjectComponent.vue'
import ContactComponent from './components/ContactComponent.vue';

</script>

<template>
  <div class="">
      <header class=" sticky top-0 z-50">
        <NavBar/>
      </header>
      <section>
        <HomeComponent/>
        <AboutComponent/>
        <ProjectComponent/>
      </section>
      <footer>
        <ContactComponent/>
      </footer>
  </div>
</template>

