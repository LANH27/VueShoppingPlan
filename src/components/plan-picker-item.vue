<template>
    <div 
    @click="select"
    :class="{'selected-plan':selected}" 
    class="plan">
        <div class="description">
          <span class="title">
            {{ name }} 
          </span>
        </div>
      </div>
    </template>

<script setup>
import { computed } from 'vue';



//Creando un evento
const emit = defineEmits(['select']);
const props = defineProps ({
    name: {
    type: String,
    required: true
    },
    selectPlan: {
      type: String
    },
});


const select = () => {

//Detomando el evento
  emit('select', props.name);
}
// creando propiedad computada
const selected = computed (() => {
  return props.name === props.selectPlan;
});
</script>
<style scoped>
.selected-plan {
  background-color: aqua;
}
</style>


