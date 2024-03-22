

<!-- Javascript -->
<script>

  export default {

   props:{
      image: String,
      brand: String,
      name: String,
      price: String,
      priceWithoutDiscount: String
   },

    data(){
      return{
        
      }
    },

    methods:{

    }

   }
</script>



<!-- HTML -->
<template>
  
   <div class="card">
      <div class="card-inside">

         <div class="upper">
            <img :src="image" alt="">
         </div>

         <div class="under">
            <p>{{ brand }}</p>
            <h2>{{ name }}</h2>

            <div class="flex">
               <p class="price">{{ price }} &euro;</p>
               <p>b</p>
            </div>
         </div>

      </div>
   </div>

</template>




<!-- CSS -->
<style lang="scss" scoped>

@use '../../assets/scss/partials/variables';



.card{
  width: calc(100% / 3);
  background-color: aliceblue;
  height: 730px;
  border: 1px solid;
  margin-bottom: 70px;

  .card-inside{
    padding: 20px;
  }
}

p{
   font-size: 18px;
}

.price{
   color: red;
   font-weight: 600;
   margin-right: 10px;
}

</style>