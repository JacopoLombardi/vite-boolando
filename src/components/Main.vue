

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
    <section class="flex">

      <div class="card">
        <div class="card-inside">


          

        </div>
      </div>


    </section>
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

section{
  background-color: beige;
  margin-top: 50px;
  width: 75%;
  height: auto;
  flex-wrap: wrap;
  justify-content: center;
  justify-content: space-evenly;
}

.card{
  width: calc(100% / 3);
  height: 500px;
  background-color: aliceblue;
  border: 1px solid;
  margin-bottom: 70px;

  .card-inside{
    padding: 20px;
  }
}

</style>