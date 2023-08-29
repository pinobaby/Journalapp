<template>
    <div class="entry-container mb-3 pointer p-2"
        @click="$router.push({ name: 'entry', params: { id: 10}})">
         <div class="entry-tittle- d-flex">

         <span class="text-success fs-5 fw-bold">{{ id }}</span>
         <span class="mx-1 fs-5">{{ date }}</span>
         <span class="mx-2 fw-light">{{ content }}</span>
        
            
        </div>  
        <div class="entry-description">
        Enim sint mollit occaecat amet labore deserunt magna occaecat ut irure esse anim. Labore dolor sit sit officia magna elit adipisicing nisi pariatur ex adipisicing anim amet cillum. Consectetur proident nisi adipisicing sunt do commodo sunt amet irure sit adipisicing occaecat officia dolore. Ex do irure proident elit.
        </div> 
   
   </div>
</template>

<script>
import {mapGetters} from 'vuex'
export default {
   props:{
         id: {
              type: [String, Number],
              required: true
         },
         date: {
              type: String,
              required: true
         },
         content: {
              type: String,
              required: true
         },
         picture: {
              type: String,
              required: false
         }
    },
    computed: {
        ...mapGetters('journal',['getEntriesByTerm']),

        EntriesByTerm () {
            return this.getEntriesByTerm(this.term)
        },
    },
    data() {
        return {
            term:''
        }
    },

   }





</script>



<style lang="scss" scoped>
      .entry-container{
        border-color: 1px solid #2c3e50;
        transition: 0.2s all ease-in;

        &:hover{
            background-color: lighten($color: grey, $amount: 45);
            
        }
        .entry-description{
            font-size: 12px;
        }
    }
</style>
