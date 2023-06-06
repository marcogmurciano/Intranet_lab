<template>

    <div class="bg flex p-2 pl-0 w-fit gap-2 h-fit">
        <div class="status_bar flex flex-col items-center" v-if="active">
            <div class="circle rounded-full w-3 h-3 bg-primary"></div>
            <div class="line border-dashed border-l-primary w-0 h-full"></div>
        </div>
        <div class="status_bar flex flex-col items-center" v-else>
            <div class="circle rounded-full w-3 h-3 bg-gray3"></div>
            <div class="line border-dashed border-l-gray3 w-0 h-full"></div>
        </div>
        <div class="main flex flex-col gap-3 pb-2">
            <div class="top flex flex-col gap-1">
                <div class="h4" v-if="title">
                    <slot />
                </div>
                <div class="h4" v-if="!title" > {{ $props.stage }}</div>
                <div class="mini" v-if="active">Hoy, a las 22.00</div>
            </div>

            <div class="bottom flex gap-2 items-center">
                <div class="title"  v-if="title">
                    <div class="cuerpo desta">En proceso</div>
                </div>
                <div class="notitle" v-else>
                    <div class="cuerpo desta" v-if="active">Completado</div>
                    <div class="cuerpo desta" v-if="!active">En proceso</div>
                </div>
                <div class="icon" v-if="title">
                    <ph-caret-down :size="16"/>
                </div>
            </div>
        </div>
    </div>
</template>


<script setup>
import { PhCaretDown } from "@phosphor-icons/vue";
    defineProps({
        title: Boolean,
        active: Boolean,
        stage: String,
    })

    

</script>


<style lang="sass" scoped>
// *
//     border: 1px solid tomato
.line
    border-left-width: 3.5px
    
</style>