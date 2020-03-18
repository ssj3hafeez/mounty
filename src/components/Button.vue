<template>
<div id= "button">
    <p @click="switchView">Switch view</p>
    
    </div> 
    
</template>

<script>
export default {
    name: "Button",
      methods: {
          switchView(){
              this.$root.$emit('switch');
          }
          }
      }
  

</script>


<style scoped>

#button{

        padding: 30px;
        border: 3px solid black;
           display: inline-block;
}


</style>