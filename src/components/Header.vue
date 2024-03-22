

<!-- Javascript -->
<script>
  export default {
    data(){
      return{
        sizesArray: [
         'Donna',
         'Uomo', 
         'Bambino'
         ],

        iconArray: [
         'icon-start-menu  fa-regular  fa-user', 
         'icon-start-menu  fa-regular  fa-heart', 
         'icon-start-menu  fa-solid  fa-bag-shopping  icon-white'
         ],
      };
    },

    methods:{

    },
  }
</script>




<!-- HTML -->

<!-- v-for="(size, index) in sizes" :key= 'index' -->
<template>

<header class="flex fixed">
   <section class="start-menu flex">
      <div class="categoria">
         <ul class="flex">
            <li v-for="(size, i) in sizesArray" :key= 'i'>
               <a class="selezione" href="#">{{ size }}</a>
            </li>
         </ul>
      </div>

      <div>
         <img class="logo" src="/public/img/boolean-logo.png">
      </div>

      <div>
         <ul class="flex">
            <li v-for="(icon, i) in iconArray" :key= 'i'>
               <a href="#">
                  <i :class="icon"></i>
               </a>
            </li>
         </ul>
      </div>
   </section>
</header>

</template>




<!-- CSS -->
<style lang="scss" scoped>

@use '../assets/scss/partials/variables' as *;


header{
   width: 100%;
   height: auto;
   background-color: $bg-header;
   justify-content: center;
   z-index: 1;
   top: 0;

   .start-menu{
      width: 1450px;
      margin: 20px;
      justify-content: space-between;
      align-items: center;
   }
}

.categoria .selezione{
   margin: 0 10px;
   font-weight: 600;
   font-size: 18px;
   text-decoration: none;

   &:hover{
      text-decoration: underline;
   }
}

.logo{
   width: 200px;
   
   &:hover{
      cursor: pointer;
   }
}

.icon-start-menu{
   font-size: 24px;
   margin: 0 8px;
   
   &:hover{
      color: darken($color: $prymary-text-color, $amount: 15%);
   }
}

</style>