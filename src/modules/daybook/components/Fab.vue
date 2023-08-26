<template class="btn btn-primary">
  <button>
    <i  class="fa fa-x2"
       :class="icon">
    </i>
  </button>
</template>
<script>
export default {
    
    props:{
        icon: {
            type: String,
            default: ' fa-plus'
            
        }
    },

}
</script>
<style lang="scss" scoped>
  button{
    background-color: #2c3e50;
    border-radius: 100%;
    bottom:    20px;
    height:    80px;
    position: fixed;
    right:     20px;
    width:     80px;
    color: rgb(255, 255, 255);
  }  
</style>