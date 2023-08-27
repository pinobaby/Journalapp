
<template lang="">
    
  <div class="entry-list-container">
    <div class="px-2 pt-2">
        <input
            type="text"
            class="form-control"
            placeholder="Buscar entrada"
        />
    </div>

    <div class="entry-scrollarea">
        <Entry
             v-for="item in getEntryesByTerm"
            :key="item"
        />
    </div>
  </div>
</template>

<script>

import { defineAsyncComponent } from 'vue'
import {mapGetters} from 'vuex'
export default {
    
    components:{
        Entry: defineAsyncComponent(() => import('../components/Entry.vue')),
    },
    computed: {
        ...mapGetters(['daybook','getEntryesByTerm'])
    },
}
</script>

<style lang="scss" scoped>

imput {
    height: 34px;
}
.entry-list-container {
    border-right: 1px solid #2c50;
    height: calc(100vh - 56px);
}

.entry-scrollarea {
    height: calc(100vh - 110px );
    overflow-y: scroll;
}
</style>
