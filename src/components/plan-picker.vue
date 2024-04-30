<template>
   <div ref="plansWrapper" style="border: red double 10px;"   class="plans">
     <plan-picker-item 
     @select="selectedPlan"
     v-for="plan in plans"
     :name="plan"
     v-bind:key="plan" />
     <p style="font-size: 38px;">Counter: {{ counter }}</p>
    </div>
</template>

<script setup>
import { ref, onMounted }  from 'vue';
import planPickerItem from './plan-picker-item.vue';
const plans=ref([
  "El soltero",
  "El adicto",
  "El viajero", ]);

  const plansWrapper = (null);

const selectedPlan = ref(null);

const printSelected = (playload) => {
  selectedPlan.value = playload; 
};

//Creando una referencia reactiva
//para un contador
const counter = ref(0);
//Creando un metodo para incrementar el contador
const processID = setInterval(() => {
  console.log('Incrementando contador');
  counter.value++;
}, 1000);
//Registrando el CB (Call Back) onMounted
onMounted(() => {
  console.log(plansWrapper.value);
  //console.log(plansWrapper.value);
});

//Registrando el CB de onMounted
onMounted(() => {
  console.log('componente Plan Piker desmontada');
  clearInterval(processID )
});
</script>

