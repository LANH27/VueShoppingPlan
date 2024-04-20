<template>
   <div class="plans">
     <plan-picker-item 
     v-for="plan in plans"
     :name="plan"
     v-bind:key="plan" />
    </div>
</template>

<script setup>
import { ref } from 'vue';
import planItem from './plan-picker-item.vue';
const plans = ref([
  "El soltero",
  "El adicto",
  "El viajero",
  "El Colombiano"]);
//Componentes Subtitulo
import vue from 'vue';

function Viajes(props) {
    return <h2>{props.viajes}</h2>;
}

export default 

</script>

