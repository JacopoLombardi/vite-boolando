

<!-- Javascript -->
<script>

  // importo dentro Main il componente Card
  import Card from './partials/Card.vue'

  // importo il file Object con i dati delle Card
  import objectCard from '../assets/jsFolder/db.json'

  export default {
    components:{
      Card
    },

    data(){
      return{
        objectCard,
      };
    },

    methods:{

    },

    mounted(){
      console.log(objectCard)
    }
  };
</script>



<!-- HTML -->
<template>
  
  <main class="flex">
    
    <Card />

  </main>
  
</template>




<!-- CSS -->
<style lang="scss" scoped>

@use '../assets/scss/partials/variables' as *;


main{
  background-color: aqua;
  margin-top: 88px;
  height: 800px;
  justify-content: center;
}

</style>