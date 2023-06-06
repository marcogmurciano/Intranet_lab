<template>
    <title>Talleres abiertos</title>
    <div class="app flex">
        <LeftSidebar where="talleres" class="w-[19%] sticky"/>
        <div class="main flex flex-col gap-6 w-full px-5 py-6">
            <div class="h1">
                Talleres abiertos
            </div>
            <div class="panel grid grid-cols-3 gap-4">
                <CardBig fecha="22/06/23"> Taller de fotografía</CardBig>
                <CardBig fecha="26/04/23"> Taller de fabricación digital</CardBig>
                <CardBig fecha="10/05/23"> Anuario</CardBig>
                <CardBig fecha="12/06/23"> Video promocional ESD</CardBig>
                <CardBig fecha="17/05/23"> Taller de costura</CardBig>
                <CardBig fecha="24/04/23"> Entre árboles</CardBig>
                <CardBig fecha="8/05/23"> Microsite</CardBig>
                <CardBig fecha="19/04/23"> Taller de carpintería</CardBig>
                <CardBig fecha="5/06/23"> Taller de estampación</CardBig>
                
                
                
            </div>
        </div>
        <RightSidebar class="w-[19%] sticky" />

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

            <MisCursos name="contenido" type="active"> <ph-notebook :size="28" /> </MisCursos>
            <MisCursos name="si no toco en una" type="default"> <ph-notebook :size="28" /> </MisCursos>

            <Notificacion type="peque"> notificando co </Notificacion>
            <Notificacion type="grande" active="false"> rabo </Notificacion>

            <CardProceso :title="true" :active="true"> </CardProceso>
            <CardProceso :title="false" :active="false"> </CardProceso>
            <CardProceso :title="false" :active="true"> </CardProceso>

            <UserPanel :type="sombra"/>
           -->
</template>


<script setup>

    //USAR FOSFORAICON html:

    // <PhAperture :size="52" color="hotpink" weight="light"> </PhAperture>
    // esto anterior es para definir propiedades de un icono en concreto
    // <PhAperture> </PhAperture>

    //USAR FOSFORAICON js:

    import { PhNotebook } from "@phosphor-icons/vue";

    // provide("color", "limegreen")
    // provide("size", 32)
    // provide("weight", "bold")
    // provide("mirrored", false)
    //esto es para definir las características de todos los iconos de la page

</script>

<style lang="sass" scoped>


</style>