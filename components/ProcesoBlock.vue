<template>
    <div class="bg" @click="toggleOpen">
        <div class="open flex flex-col gap-3" v-if="ropen">
        <div class="title flex items-center gap-1">
            <div class="h4"> {{ props.title }} </div>
            <ph-caret-up :size="16" />
        </div>
        <CardProceso :title="false" :active="true" stage="Solicitud enviada"> </CardProceso>
        <CardProceso :title="false" :active="false" stage="Solicitud recibida"> </CardProceso>
        <CardProceso :title="false" :active="false" stage="Resolución"> </CardProceso>
    </div>
    <div class="closed" v-else>
        <CardProceso :title="true" :active="true"> {{ props.title }} </CardProceso> 
        
    </div>
    </div>
</template>


<script setup>
const props = defineProps ({
 title: String,
 open: Boolean,
})

const ropen = ref(props.open)

const toggleOpen = () => {
    ropen.value = !ropen.value
}

import { PhCaretUp } from "@phosphor-icons/vue";
</script>


<style lang="sass" scoped>

</style>