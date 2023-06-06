<template>
    <div class="bg">
        <div class="card_top flex justify-between">
            <slot />
            <div class="h3"> {{ title }} </div>
        </div>
        <div class="card_down flex justify-between">
            <div class="notas">plazo</div>
            <div class="notas">{{ plazo }}</div>
        </div>
    </div>
</template>


<script setup>
defineProps({
    title: String,
    plazo: String,
})
</script>


<style lang="sass" scoped>
    .card_down
        border-top: 1px solid  
        @apply pt-2
    .bg
        @apply flex flex-col gap-7 rounded-lg bg-white px-9 py-2 shadow-normal
    .bg:hover
        @apply shadow-hover
    
</style>