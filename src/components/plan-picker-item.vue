<template>
    <div class="plan">
        <div class="description">
          <span class="title">
            {{ name }} 
          </span>
        </div>
      </div>
    </template>

<script setup>

//Componentes plan-picker;
import vue from 'vue';

function planPicker(props) {
return (
  <div>
  <h3>Planes Disponibles </h3>
  <ul>
     {props.planes.map((plan, index )=>(
      <li key={index}>{plan}</li>
     ))}
     </ul>
    </div>
);
  }

defineProps ({
    name: {
    type: String,
    required: true
    }
});
</script>


