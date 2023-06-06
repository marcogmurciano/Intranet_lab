<template>
    <title>Matrícula</title>
    <div class="app flex">
        <LeftSidebar where="matricula" class="w-[19%]"/>
        <div class="main flex flex-col gap-6 w-full px-5 py-6">
            <div class="h1">
                Matrícula
            </div>
            <div class="panel grid grid-cols-2 gap-4">
                <NuxtLink to="/TalleresHome"> <CardLittle title="Plazos generales" plazo="27 de Mayo"> <ph-file-search :size="28" /> </CardLittle> </NuxtLink>
                <CardLittle title="Instrucciones de matrícula" plazo="16 de Abril"> <ph-file :size="28" /> </CardLittle>
                <CardLittle title="Gestión de matrícula" plazo="12 de Junio"> <ph-file-text :size="28" /> </CardLittle>
                <CardLittle title="Información de matrícula" plazo="22 de Abril"> <ph-file-plus :size="28" /></CardLittle>
                
            </div>
        </div>
        <RightSidebar class="w-[19%]"/>

        

    </div>
    
            <!-- 
            CHULETA COMPONENTES
            
            <CardLittle title="Gestión de polladas" plazo="27 de Mayo"> <PhAperture :size="28"/> </CardLittle>
            <CardLong clas="3ro" curso="2022/23" prof="La Hector"> titulo de alargated card tu sabes </CardLong>
            <CardBig fecha="20/07/22"> titulo de gran card </CardBig>
            <Calendar />
            <ModalWindow />
            <Formulario type="dropdown"/>
            <Formulario type="bigOne"/>
            <Formulario type="default"/> 


            <Button type="primary"> botonaco yea</Button>
            -->
</template>


<script setup>

    import { PhFile } from "@phosphor-icons/vue";
    import { PhFileSearch } from "@phosphor-icons/vue";
    import { PhFileText } from "@phosphor-icons/vue";
    import { PhFilePlus } from "@phosphor-icons/vue";
   

    //USAR FOSFORAICON html:

    // <PhAperture :size="52" color="hotpink" weight="light"> </PhAperture>
    // esto anterior es para definir propiedades de un icono en concreto
    // <PhAperture> </PhAperture>

    //USAR FOSFORAICON js:

    

    // provide("color", "limegreen")
    // provide("size", 32)
    // provide("weight", "bold")
    // provide("mirrored", false)
    //esto es para definir las características de todos los iconos de la page

</script>

<style lang="sass" scoped>


</style>




