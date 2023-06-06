<template>
    <div class="bg flex flex-col px-6 pt-[84px] gap-6 border-gray2 border-l">
        <Calendar></Calendar>
        <div class="bloque">
            <Notificacion type="peque"> Taller en 1 hora </Notificacion>
            <Notificacion type="grande"> Mañana entrega de Proyectos </Notificacion>
        </div>
        <div class="bloque">
            <ProcesoBlock title="Cagar en el esc" :open="false"/>
        </div>
    </div>
</template>


<script setup>

</script>


<style lang="sass" scoped>
    .bloque
        @apply flex flex-col gap-3
</style>