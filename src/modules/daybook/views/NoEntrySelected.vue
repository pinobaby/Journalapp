<template lang="">
    <div class="d-flex justify-content-center">
        <h1 class="align-self-center">No hay nada seleccionado</h1>
    </div>

    <fab />
</template>
<script>
import { defineAsyncComponent } from 'vue'
export default {
    components: {
        fab: defineAsyncComponent(() => import(/* webpackChunkName: "fab" */ '../components/Fab.vue')),
    },
}
</script>
<style lang="scss" scoped>
    div {
        height: 100%;
    }
</style>