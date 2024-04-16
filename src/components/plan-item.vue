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
const props = defineProps(['name']);
console.log(props.name);
</script>

