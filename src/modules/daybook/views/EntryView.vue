import { defineAsyncComponent } from 'vue';
<template lang="">
    <div class="entry-title d-flex justify-content-between p-2">
        <div>

            <span class= "text-success fs-3 fw-bold">23</span>
            <span class= "mx-1 fs-3">agosto</span>
            <span class= "mx-2 fs-4 fw-light">2023, miercoles</span>
            
        </div>
        <div>
        <button class="btn btn-danger mx-2">
            Borrar
            <i class="fa fa-trash-alt"></i>
        </button>
        <button class="btn btn-primary">
            Subir Foto
            <i class="fa fa-upload"></i>
        </button>
        </div>
    </div>

    <hr>
    <div class="d-flex flex-column px-3 h-75">
        <textarea placeholder="¿Qué sucedio ayer?"></textarea>
        <img 
        src="../../../assets/feo.jpeg" 
        alt="Entry-picture"
        class="img-thumbnail">
        <Fab
          icon="fas fa-save"  
        />
    </div>

</template>
<script>
import { defineAsyncComponent } from 'vue';
export default {
    components: {
        Fab: defineAsyncComponent(() => import('../components/Fab.vue')),
    },
}
</script>
<style lang="scss" scoped>
    text{
        font-size: 20px;
        border: none;
        height: 100%;

        &:focus {
            outline: none;
        }

    }
    img{
        width: 200px;
        position: fixed;
        bottom: 150px;
        right: 20px;
        box-shadow: 0px 5px 10px rgba($color: black, $alpha: 0.2);
    }
</style>