<script setup>
import planPicker from './components/plan-picker.vue';
import { ref } from 'vue';
const showPlans = ref(true);
</script>

<template>
  <header>
    <div>
      <span id="logo">Liquid Gold Box</span>
      <img src="./assets/logo.png" alt="logo">
    </div>
  </header>

  <div class="content">
    <h1 class="title">Coffe Plans</h1>
    <h2 class="subtitle">
      Viajamos por el mundo para encontrar el mejor cafe de origen unico para ti 
    </h2> 
    <label>
      <input type="checkbox" v-model="showPlans">
      Mostrar Selector de Planes
    </label>
    <plan-picker v-if="showPlans" />
    
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
