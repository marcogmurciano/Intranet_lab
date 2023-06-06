<template>
    <div class="bg h-fit w-full">

        <div class="top gap-1" :class="type">
            <div :class="a">
                <slot />
            </div>
            <div class="notas middle">Es normal</div>
        </div>

        <div class="bottom">
            <div :class="b">Relacionado con <span class="desta">Matrícula</span></div>
        </div>

    </div>
</template>

<script setup>
const props = defineProps({
    type: String,
})
let b = ''
let a = ''
if (props.type == 'peque') {
    b = 'mini'
    a = 'notas'
} else if (props.type == 'grande') {
    b = 'cuerpo'
    a = 'h4'
}

</script>

<style lang="sass" scoped>
    .bg
        @apply flex flex-col px-3 py-2 gap-3 rounded border-l-primary border-l-4 w-fit

    .peque .middle
            @apply hidden
</style>