<template>
    <div class="bg">
        <div class="mini">Taller abierto</div>
        <div class="middle flex gap-1">
            <PhCalendarBlank :size="20" />
            <div class="cuerpo">Fecha:<span class="desta">  {{ fecha }}</span></div>
        </div>
        <div class="h3"> <slot /> </div>
        <Button type="primary"> Acceder </Button>
    </div>
</template>


<script setup>
import { PhCalendarBlank } from "@phosphor-icons/vue";
defineProps({
    fecha: String,
})

</script>


<style lang="sass" scoped>
    .bg
        @apply flex flex-col gap-7 rounded-lg bg-white px-2 py-2 shadow-normal
    .bg:hover
        @apply shadow-hover
</style>