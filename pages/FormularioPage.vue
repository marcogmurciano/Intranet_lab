<template>
    <title>Formulario</title>
    <div class="app flex">
        <LeftSidebar where="gestiones" class="w-[19%] sticky"/>
        <div class="modalContainer relative flex w-full">
            <ModalWindow class="absolute w-full h-full" v-if="modalCounter" />
            <div class="main flex flex-col gap-6 w-full px-5 py-6">
            <div class="h1">
                Formulario
            </div>
            <div class="panel flex flex-col gap-3">
                <div class="up flex sombra rounded">
                    <UserPanel />
                    <div class="forms flex flex-col w-full px-6 py-8">
                        <Formulario type="dropdown"> Nombre de la asignatura </Formulario>
                        <Formulario type="default"> DNI/ documento de identificación </Formulario>
                    </div>
                </div>
                <div class="down flex gap-3">
                    <div class="left w-[75%] sombra px-6 py-8 rounded">
                        <Formulario type="bigOne"> Motivo de la matriculación </Formulario>
                    </div>
                    <div class="right flex flex-col sombra bg-white px-6 py-8 gap-1 rounded">
                        <Button @click="openModal"> Enviar formulario </Button>
                        <Button> Resetear </Button>
                    </div>
                </div>
            </div>
        </div>
        <RightSidebar class="w-[19%] sticky"/>
        </div>

    </div>

    <!-- 
            CHULETA COMPONENTES
            
            <CardLittle title="Gestión de polladas" plazo="27 de Mayo"> <PhAperture :size="24"/> </CardLittle>
            <CardLong clas="3ro" curso="2022/23" prof="La Hector"> titulo de alargated card tu sabes </CardLong>
            <CardBig fecha="20/07/22"> titulo de gran card </CardBig>
            <Calendar />
            <ModalWindow />
            <Formulario type="default"> Nombre de la asignatura</Formulario> 
            default/bigOne/dropdown
           -->
</template>


<script setup>

import Formulario from '../components/Formulario.vue';


//USAR FOSFORAICON html:

// <PhAperture :size="52" color="hotpink" weight="light"> </PhAperture>
// esto anterior es para definir propiedades de un icono en concreto
// <PhAperture> </PhAperture>

//USAR FOSFORAICON js:

import { PhAperture } from "@phosphor-icons/vue";

    // provide("color", "limegreen")
    // provide("size", 32)
    // provide("weight", "bold")
    // provide("mirrored", false)
    //esto es para definir las características de todos los iconos de la page

let modalCounter= ref(false)

const openModal = () => {
    modalCounter.value = !modalCounter.value
}

</script>

<style lang="sass" scoped>


</style>




