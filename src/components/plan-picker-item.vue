<template>
    <div 
    @click="select"
    :class="{'selected-plan':selected}" 
    class="plan">
        <div class="description">
          <span class="title">
            {{ name }} ultimo seleccionado: {{ selectedPlan}}
          </span>
        </div>
      </div>
    </template>

<script setup>


//Creando un evento
const emit = defineEmits(['select']);
const prps = defineProps ({
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

</script>
<style scoped>
.selected-plan {
  background-color: aqua;
}
</style>


