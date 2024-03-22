

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
               @mouseleave="x = false"
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


            <div 
               :class="badgesRedValue === 'Sostenibilità' ? 'd-none' : ''"
               class="sconto absolute">
               {{ badgesRedValue }}
            </div>

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


p{
   font-size: 18px;
}

.card{
  width: calc(100% / 3);
  margin-bottom: 70px;

  .card-inside{
    padding: 20px;
  }
}

.price{
   color: $danger-color;
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

   .cuore{
      font-size: 45px;
      justify-content: center;

      &:hover{
         color: $danger-color;
         cursor: pointer;
      }
   }
   .red{
      color: $danger-color;
   }
}



// Badges
.sconto{
   background-color: $danger-color;
}

.sostenibile{
   background-color: $safe-color;
   left: 15%;
}

.sconto,
.sostenibile{
   color: $prymary-text-color;
   font-weight: 600;
   padding: 5px 10px;
   text-align: center;
   bottom: 8%;
}

</style>