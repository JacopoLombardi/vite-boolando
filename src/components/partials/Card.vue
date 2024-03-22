

<!-- Javascript -->
<script>

  export default {

   props:{
      imageShowed: Image,
      imageHidden: Image,

      brand: String,
      name: String,
      price: Number,
      
      isInFavorites: Boolean,

      badgesRedType: String,
      badgesRedValue: String,

      badgesGreenType: String,
      badgesGreenValue: String
   },

    data(){
      return{
        
      }
    },

    mounted(){
      
    }

   }
</script>



<!-- HTML -->
<template>
  
   <div class="card">
      <div class="card-inside">

         <div class="upper  relative">
            <div
               @mouseover="x = true"
            >
               <img 
                  :class="x === true ? 'd-none' : ''" 
                  :src="imageShowed" 
                  :alt="brand">

               <img 
                  :class="x === true ? 'd-inline-block' : 'd-none'" 
                  :src="imageHidden" 
                  :alt="brand"
               >
            </div>

            <div class="scatola-cuore absolute flex">
               <span 
                  :class="{'red': isInFavorites === true}" 
                  class="cuore flex">
                  &hearts;
               </span>
            </div>

            <div class="sconto absolute">{{  }}</div>

            <div 
               v-if="badgesGreenValue === 'Sostenibilità'"
               class="sostenibile absolute">
               Sostenibile
            </div>
         </div>

         <div class="under">
            <p>{{ brand }}</p>
            <h2>{{ name }}</h2>
            <p class="price">{{ price }} &euro;</p>
         </div>

      </div>
   </div>

</template>




<!-- CSS -->
<style lang="scss" scoped>

@use '../../assets/scss/partials/variables' as *;



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


// Heart
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
   cursor: pointer;
}

.red{
   color: red;
}

.cuore:hover{
   color: red;
}


// Tag
.sconto{
   color: $prymary-text-color;
   font-weight: 500;
   text-align: center;
   background-color: $danger-color;
   padding: 5px;
   width: 60px;
   bottom: 8%;
}

.sostenibile{
   color: $prymary-text-color;
   font-weight: 600;
   text-align: center;
   background-color: $safe-color;
   padding: 5px;
   width: 100px;
   bottom: 8%;
   left: 14%;
}

</style>