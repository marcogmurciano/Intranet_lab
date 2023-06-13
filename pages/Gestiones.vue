<template>
    <title>Mis Gestiones</title>
    <div class="app flex">
        <LeftSidebar where="gestiones" class="w-[19%]"/>
        <div class="main flex flex-col gap-6 w-full px-5 py-6">
            <div class="h1">
                Mis Gestiones
            </div>
            <div class="panel grid grid-cols-2 gap-4">
                <CardLittle title="Consultar expediente" plazo="22 de Mayo"> <ph-file-plus :size="28" /> </CardLittle>
                <CardLittle title="Asistencia" plazo="17 de Abril"> <ph-user :size="28" /> </CardLittle>
                <CardLittle title="Anulación beca" plazo="12 de Junio"> <ph-coin :size="28" /> </CardLittle>
                <NuxtLink to="/GestionesMatricula"> <CardLittle title="Gestiones de matrícula" plazo="31 de Mayo"> <ph-file-plus :size="28" /> </CardLittle> </NuxtLink>
                <CardLittle title="Calificaciones" plazo="6 de Junio"> <ph-bookmark-simple :size="28" /> </CardLittle>
            </div>
        </div>
        <RightSidebar class="w-[19%]"/>

    </div>
    
            <!-- 
            CHULETA COMPONENTES
            
            <CardLittle title="Gestión de polladas" plazo="27 de Mayo"> <PhAperture :size="24"/> </CardLittle>
            <CardLong clas="3ro" curso="2022/23" prof="La Hector"> titulo de alargated card tu sabes </CardLong>
            <CardBig fecha="20/07/22"> titulo de gran card </CardBig>
            <Calendar />
            <ModalWindow />
            <Formulario type="dropdown"/>
            <Formulario type="bigOne"/>
            <Formulario type="default"/> 
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

</script>

<style lang="sass" scoped>


</style>