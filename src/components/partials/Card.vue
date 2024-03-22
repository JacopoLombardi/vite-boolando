

<!-- Javascript -->
<script>

  export default {

   props:{
      image: String,
      brand: String,
      name: String,
      price: Number,
      priceWithoutDiscount: String
   },

    data(){
      return{
        
      }
    },

   }
</script>



<!-- HTML -->
<template>
  
   <div class="card">
      <div class="card-inside">

         <div class="upper  relative">
            <div>
               <img :src="image" :alt="brand">
            </div>

            <div class="scatola-cuore absolute flex">
               <span class="cuore flex">&hearts;</span>
            </div>
         </div>

         <div class="under">
            <p>{{ brand }}</p>
            <h2>{{ name }}</h2>

            <div>
               <p class="price">{{ price }} &euro;</p>
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


.scatola-cuore{
   width: 60px;
   height: 60px;
   background-color: white;
   display: block;
   top: 5%;
   right: 0;
}

.cuore{
   font-size: 45px;
   justify-content: center;
}

.cuore:hover{
   color: red;
}

</style>