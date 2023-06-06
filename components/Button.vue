<template>
    <button :class="type" class="cuerpo">
        <slot />
    </button>
</template>


<script setup>
    defineProps({
        type: String,
    })
</script>


<style lang="sass" scoped>
    .cuerpo
        @apply p-4 rounded-lg text-gray-100 px-4 py-2 
        width: fit-content
    .primary
        @apply bg-primary
    .secondary
        @apply bg-light
</style>