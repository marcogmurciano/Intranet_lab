<script setup>

import { defineProps } from 'vue';

const props = defineProps({
  type: String,
  
});
    let formclass = ''
    let dropclass = ''
    if (props.type=='dropdown') {
        formclass = 'hidden'
        dropclass = 'flex flex-col'
    }else if (props.type == 'bigOne') {
        formclass = props.type
        dropclass = 'hidden'
    }else if (props.type == 'default') {
        formclass = props.type
        dropclass = 'hidden'
    }
    
</script>

<template>
    <form class="w-full" action="">
        <div class="notas flex flex-col gap-4">
            <slot />
        </div>
        <div :class="formclass" class="form_down justify-between">
            <input type="text" placeholder="Esto es un pleisjolder">
            <img src="../public/sample_icon.svg" alt="" class="w-5 h-5">
        </div>
        <div :class="dropclass" class="dropdown w-full align-bottom">

            <div class="form_title flex justify-between">
                <img src="../public/sample_icon.svg" alt="" class="w-5">
                <div class="group flex gap-1">
                    <div class="cuerpo">
                        Selecciona la fecha
                    </div>
                    <img src="../public/sample_icon.svg" alt="" class="w-5">
                </div>
            </div>

            <div class="select_container flex justify-end w-full">
                <select name="Selecciona fecha" id="" class="">
                    <option value="1">10/01/22</option>
                    <option value="2">10/02/22</option>
                    <option value="3">10/03/22</option>
                    <option value="4">10/04/22</option>
                    <option value="5">10/05/22</option>
                </select>
            </div>
        </div>
    </form>
</template>

<style lang="sass" scoped>

    .default
        @apply border-b border-gray3 flex
       
    .bigOne
        @apply border-t border-l border-gray3 flex
  
    input
        background-color: transparent
        border: none
        outline: none
        box-shadow: none
        @apply text-blacko

    input[type="text"]::placeholder
        @apply text-gray3 
        font-family: 'Poppins'
        font-weight: 300
        line-height: 24px
        font-size: 15px
    select
        appearance: none
        @apply pr-6 bg-transparent
        
        outline: none
        color: #333333
        width: 200px
        height: 30px
        margin-bottom: 10px
        option
            @apply text-white
            font-family: 'Poppins'
            font-weight: 300
            line-height: 24px
            font-size: 15px
            background: #222222
        

            
</style>


