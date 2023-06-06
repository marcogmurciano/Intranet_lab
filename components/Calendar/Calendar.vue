<template>
    <div class="bg">
        <div class="calendar_top flex px-2 justify-between">
            <div class="h5">Marzo</div>
            <div class="icon_group flex gap-2">
                <ph-caret-left :size="16" />
                <ph-caret-right :size="16" />


            </div>
        </div>
        <div class="calendar_body flex flex-col gap-1">
            <div class="row">
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
            </div>
            <div class="row">
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
            </div>
            <div class="row">
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
            </div>
            <div class="row">
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
            </div>
            <div class="row">
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
                <CalendarTiles :state="array[random()]" :num="calendarPlusOne()" />
            </div>
        </div>
    </div>
</template>


<script setup>

import { PhCaretRight } from "@phosphor-icons/vue";
import { PhCaretLeft } from "@phosphor-icons/vue";

import CalendarTiles from './CalendarTiles.vue';

const array = [
    'inactive',
    'today',
    'delay',
    'default',
    'default',
    'default',
    'default',
    'default',
    'default',
    'default',
    'default',
    'default',
    'default',
    'default',
    'default',
    'deadline',
    'event',
]

let calendarNumber = 0

let inactiveCounter = 0


const random = () => {
    if (calendarNumber == 30){
        inactiveCounter++
    }
    if (inactiveCounter == 1) {
        return 0
    } else {
        const aleatorio = Math.floor(Math.random() * array.length)
        return aleatorio
    }
    
}



const calendarPlusOne = () => {
    calendarNumber++
    if (calendarNumber == 31) {
        calendarNumber = calendarNumber-30
    }
    return calendarNumber
}

</script>


<style lang="sass" scoped>
    .row
        @apply flex gap-0.5
    .calendar_body
        @apply pt-2
        border-top: #BCBCBC solid 1px 
    
        
</style>
