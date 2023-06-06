<template>
    <div class="bg">
        <div class="h3"> <slot /> </div>
        <div class="middle flex">
            <div class="box">
                <div class="h4">{{ clas }}</div>
                <div class="mini">clase</div>
            </div>
            <div class="box">
                <div class="h4">{{ curso }}</div>
                <div class="mini">curso</div>
            </div>
            <div class="box">
                <div class="h4">{{ prof }}</div>
                <div class="mini">profesor</div>
            </div>
        </div>
    </div>
</template>


<script setup>
defineProps({
    clas: String,
    curso: String,
    prof: String,
})
</script>


<style lang="sass" scoped>
    .bg
        @apply flex flex-row gap-9 rounded-lg bg-white px-2 py-2 justify-between items-center shadow-normal

    .bg:hover
        @apply shadow-hover
    .box
        @apply flex flex-col pl-6 pr-6
        border-left: solid 1px #000  
</style>