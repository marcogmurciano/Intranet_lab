<script setup>
    import { PhNotebook } from "@phosphor-icons/vue";
    import { PhUserCircle } from "@phosphor-icons/vue";
    import { PhLaptop } from "@phosphor-icons/vue";
    import { PhArchiveBox } from "@phosphor-icons/vue";
    import { PhCalendarBlank } from "@phosphor-icons/vue";
    import { PhFile } from "@phosphor-icons/vue";
    import { PhFiles } from "@phosphor-icons/vue";
    import { PhUsers} from "@phosphor-icons/vue";
    import { PhPuzzlePiece } from "@phosphor-icons/vue";
    import { PhGearSix } from "@phosphor-icons/vue";

    const props = defineProps({
        where: String,
    })

    let locationArray = [
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
    ]


    if (props.where=='perfil') {
        locationArray.unshift(true);
    } else if (props.where=='talleres'){
        locationArray.splice(1, 0, true);
    }else if (props.where=='cursos'){
        locationArray.splice(2, 0, true);
    }else if (props.where=='gestiones'){
        locationArray.splice(3, 0, true);
    }else if (props.where=='horario'){
        locationArray.splice(4, 0, true);
    }else if (props.where=='matricula'){
        locationArray.splice(5, 0, true);
    }else if (props.where=='eventos'){
        locationArray.splice(6, 0, true);
    }else if (props.where=='practicas'){
        locationArray.splice(7, 0, true);
    }else if (props.where=='burocracia'){
        locationArray.splice(8, 0, true);
    }else if (props.where=='ajustes'){
        locationArray.push(true);
    }


</script>


<template>
    <div class="bg-gray1 flex flex-col gap-7 p-6">
        <div class="top flex flex-col gap-1 justify-center items-center">
            <div class="userpic rounded-full bg-gray4 w-[40px] h-[40px]"></div>
            <div class="h4">Benito C.</div>
            <div class="mini text-gray4">bcamela4176@esdmadrid.es</div>
        </div>
        <div class="menu flex flex-col gap-3">
            <MisCursos name="Mi perfil" :active="locationArray[0]"> <ph-user-circle :size="28" /> </MisCursos>
            <NuxtLink to="/TalleresHome"><MisCursos name="Talleres abiertos" :active="locationArray[1]"> <ph-laptop :size="28" /></MisCursos> </NuxtLink>
            <MisCursos name="Mis cursos" :active="locationArray[2]"> <ph-notebook :size="28" /> </MisCursos>
            <NuxtLink to="/Gestiones"><MisCursos name="Mis gestiones" :active="locationArray[3]"> <ph-archive-box :size="28" /> </MisCursos> </NuxtLink>
            <MisCursos name="Horario general" :active="locationArray[4]"> <ph-calendar-blank :size="28" /> </MisCursos> 
            <NuxtLink to="/"><MisCursos name="Matrícula" :active="locationArray[5]"> <ph-file :size="28" /> </MisCursos></NuxtLink>
            <MisCursos name="Eventos" :active="locationArray[6]"> <ph-users :size="28" /> </MisCursos>
            <MisCursos name="Prácticas" :active="locationArray[7]"> <ph-puzzle-piece :size="28" /> </MisCursos>
            <MisCursos name="Burocracia" :active="locationArray[8]"> <ph-files :size="28" /> </MisCursos>
            <MisCursos name="Ajustes" :active="locationArray[9]"> <ph-gear-six :size="28" /> </MisCursos>

        </div>
    </div>
</template>



<style lang="sass" scoped>
  
</style>