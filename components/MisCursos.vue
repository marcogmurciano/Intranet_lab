<template>
    <div class="main flex items-center" @click="activeToggle()">
        <div class="icon">
            <slot />
        </div>
        <div class="h4 text-gray4" v-if="!active"> {{ props.name }} </div>
        <div class="h4" v-else> {{ props.name }} </div>
    </div>
</template>


<script setup>
const props = defineProps({
    name: String,
    active: Boolean,
})
const active = ref ( props.active)

let color = ''
if (active.value) {
    color = '#000000'
} else if (!active.value) {
    color = '#BCBCBC'
}

provide("color", color)

const activeToggle = () => {
    active.value = !active.value
    if (active.value) {
        color = '#000000'
    } else if (!active.value) {
        color = '#BCBCBC'
    }
}

</script>


<style lang="sass" scoped>
    .main
        @apply flex gap-1 p-2
    .main:hover
        @apply border-gray3 rounded

</style>