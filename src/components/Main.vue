

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
      
    }
  };
</script>



<!-- HTML -->
<template>
  
  <main class="flex">
    <section class="flex">
    
      <Card
        v-for="(item, i) in objectCard.products"
        :key="i"

        :imageShowed="`src/assets/img/${item.frontImage}`"
        :imageHidden="`src/assets/img/${item.backImage}`"

        :brand="item.brand"
        :name="item.name"
        :price="item.price"

        :isInFavorites="item.isInFavorites"

        :badgesRedValue="item.badges[item.badges.length - 1].value"
        :badgesGreenValue="item.badges[0].value"


      />

    </section>
  </main>
  
</template>




<!-- CSS -->
<style lang="scss" scoped>

@use '../assets/scss/partials/variables' as *;


main{
  background-color: aqua;
  margin-top: 88px;
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

</style>