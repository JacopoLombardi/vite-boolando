

<!-- Javascript -->
<script>
  export default {
    data(){
      return{
         infoArray:[
            'informazioni legali',
            'normativa sulla privacy',
            'Diritto di recesso'
         ],

         brandsArray: [
            'fa-square-twitter',
            'fa-square-facebook',
            'fa-square-instagram',
            'fa-square-pinterest',
            'fa-square-youtube'
         ],
      }
    },

    methods:{

    },
  }
</script>



<!-- HTML -->

<!--  v-for="(icon, i) in iconArray" :key= 'i' -->
<template>

<footer class="flex">
   <section class="end-menu  flex">
      <div class="informazioni">
         <h3>Boolando s.r.l.</h3>

         <ul class="flex">
            <li v-for="(info, i) in infoArray" :key= 'i'>
               <a class="info-clienti" href="#">{{ info }}</a>
            </li>
         </ul>

      </div>

      <div class="social">
         <h4>Trovaci anche su</h4>

         <ul class="lista-social  flex">
            <li v-for="(brand, i) in brandsArray" :key= 'i'>
               <a href="#">
                  <i :class="brand" 
                     class="fa-brands">
                  </i>
               </a>
            </li>
         </ul>

      </div>
   </section>
</footer>

</template>




<!-- CSS -->
<style lang="scss" scoped>

@use '../assets/scss/partials/variables' as *;


footer{
   background-color: black;
   justify-content: center;
   .end-menu{
      width: 1450px;
      margin: 0 20px;
      
      justify-content: space-between;
   }
}

.informazioni{
   color: white;
}

h3{
   margin: 30px 0 15px 5px;
}
.info-clienti{
   margin: 0 8px;
   text-decoration: none;
   &:hover{
      text-decoration: underline;
   }
}

.social .lista-social a,
.info-clienti,
h4{
   color: white;
}

.lista-social{
   list-style: none;

   flex-direction: row;
}

h4{
   text-align: center;
   margin: 30px 0 0 8px;
}

.fa-brands{
   font-size: 26px;
   margin: 15px 8px;
}

</style>