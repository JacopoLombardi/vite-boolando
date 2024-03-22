

<!-- Javascript -->
<script>

  export default {
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
  
  <section class="flex">

   <div class="card">
      <div class="card-inside">

         <div class="upper">
            <img src="../../assets/img/1.webp" alt="">
         </div>

         <div class="under">
            <p>asas</p>
            <h2>ads</h2>

            <div class="flex">
               <p class="price">a</p>
               <p>b</p>
            </div>
         </div>

      </div>
   </div>


</section>

</template>




<!-- CSS -->
<style lang="scss" scoped>



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
  height: 730px;
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


</style>