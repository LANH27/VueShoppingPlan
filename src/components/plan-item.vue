<template>
    <div class="plan">
        <div class="description">
          <span class="title">
            {{ name }} 👍 likes {{ likes }}
          </span>
        </div>
      </div>
    </template>

<script setup>
defineProps ({
    name: String,
    likes: {
        type: Number,
        default: 0,
    }
});
</script>

