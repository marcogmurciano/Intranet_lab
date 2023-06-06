<template>
  <div class="tile_container rounded" :class="state">
    <div class="cuerpo h-fit w-fit">{{ num }}</div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

defineProps({
  state: String,
  num: Number,
});
</script>


<style lang="sass" scoped>
    .tile_container
        width: 24px
        height: 24px
        @apply flex align-middle justify-center
    .default
        @apply text-blacko
    .inactive
        @apply text-gray5
    .today
        @apply text-primary
    .deadline
        @apply bg-primary text-white
    .delay
        @apply bg-malo text-white
    .event
        @apply bg-light text-white
</style>