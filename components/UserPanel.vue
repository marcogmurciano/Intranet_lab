<template>
    <div :class="type" class="bg-white flex flex-col items-center p-2 gap-2 w-fit rounded">
        <div class="top flex flex-col items-center">
            <div class="user_pic w-[83px] h-[83px] rounded-full bg-gray4"></div>
            <div class="user_data flex flex-col gap-1 items-center">
                <div class="h2">Benito C.</div>
                <div class="mini">bcamela4713@esdmadrid.es</div>
            </div>
        </div>

        <div class="bottom flex justify-between gap-14">
            <div class="curso_especialidad flex flex-col items-center gap-1">
                <div class="h4">3ro</div>
                <div class="mini">Gráfico</div>
            </div>
            <div class="alumno_usuario flex flex-col items-center gap-1">
                <div class="h4">Alumno</div>
                <div class="mini">Usuario</div>
            </div>
        </div>
        <Button type="primary"> Editar </Button>

    </div>
</template>


<script setup>

defineProps ({
    type: String,
})

</script>


<style lang="sass" scoped>


</style>