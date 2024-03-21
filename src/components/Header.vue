

<!-- Javascript -->
<script>
  export default {
    data(){
      return{
        sizesArray:['Donna', 'Uomo', 'Bambino'],
        iconArray:[
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
   <div class="start-menu flex">
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
   </div>
</header>

</template>




<!-- CSS -->
<style>

header{
   width: 100%;
   height: auto;
   background-color: rgb( 255, 105, 0);
   justify-content: center;
   z-index: 1;
   top: 0;
}

.start-menu{
   width: 1450px;
   justify-content: space-between;
   align-items: center;
   margin: 20px;
}

ul{
   list-style: none;
}

.categoria .selezione{
   margin: 0 10px;
   font-weight: 600;
   font-size: 18px;
   color: white;
   text-decoration: none;
}

.categoria .selezione:hover{
   text-decoration: underline;
}

.logo{
   width: 150px;
}

.logo:hover{
   cursor: pointer;
}

.icon-start-menu{
   color: white;
   font-size: 24px;
   margin: 0 8px;
}

.icon-start-menu:hover{
   color: rgb(226, 226, 226);
}

</style>