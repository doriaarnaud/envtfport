<script setup>
import {ref} from 'vue'
let techtab=ref(
[
    {id:0,logo:'/logos/vuejs.JPG',description:"Vue.js",title:'Vue.js logo',textalt:'vue3 logo'},
    {id:1,logo:'/logos/vite.JPG',description:"Vite",title:'Vite logo',textalt:'vite logo'},
    {id:2,logo:'/logos/vuetify.png',description:"Vuetify",title:'Vuetify logo',textalt:'vuetify logo'},
    {id:3,logo:'/logos/js.JPG',description:"JavaScript",title:'JavaScript logo',textalt:'javascript logo'},
    {id:4,logo:'/logos/css3.JPG',description:"css3",title:'css3 logo',textalt:'css3 logo'},
    {id:5,logo:'/logos/html5.JPG',description:"html5",title:'html5 logo',textalt:'html5 logo'}
]);
</script>
<template>
  <div class="tech2content">
    <v-card class="pb-8" color="#09090d">
       <h1 class="techtitle ms-5 mt-5 h-auto">Technologies</h1>
         <div class="techimages">
             <div class="techcontent ma-4" v-for="images in techtab" :key="images.id">
                 <img :src="images.logo" :alt="images.textalt" :title="images.title" width="100" height="100"/>
                 <div class="imagetitle">
                     <h1 class="text-h6">{{ images.description }}</h1>
                 </div>
             </div>
         </div>
    </v-card>
  </div>
</template>

<script>
</script>

<style>
  @media (min-width: 1200px)
  {
    .tech2content
    {
      position:relative;
      width:100%;
      padding-top:0px;
      margin-left:auto;
      margin-right:auto;
    }
    .techimages
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: center;
      margin-top: 50px;
    }
    .techcontent
    {
      margin-top:10px;
      padding:10px;
    }
    .techcontent img
    {
      border-radius: 15px;
    }
  }
  @media (min-width: 992px) and (max-width: 1199px)
  {
    .tech2content
    {
      position:relative;
      width:100%;
      min-height:350px;
      padding-top:0px;
    }
    .techimages
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: center;
      margin-top: 50px;
    }
    .techcontent
    {
      margin-top:10px;
      padding:10px;
    }
    .techcontent img
    {
      border-radius: 15px;
    }
  }
  @media (min-width: 768px) and (max-width: 991px)
  {
    .tech2content
    {
      position:relative;
      width:100%;
      min-height:350px;
      padding-top:0px;
    }
    .techimages
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: center;
      margin-top: 50px;
    }
    .techcontent
    {
      margin-top:10px;
      padding:10px;
    }
    .techcontent img
    {
      border-radius: 15px;
    }
  }
  @media (min-width: 576px) and (max-width: 767px)
  {
    .tech2content
    {
      position:relative;
      width:100%;
      min-height:350px;
      padding-top:0px;
    }
    .techimages
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: center;
      margin-top: 50px;
    }
    .techcontent
    {
      margin-top:10px;
      padding:10px;
    }
    .techcontent img
    {
      border-radius: 15px;
      width:70px;
      height:70px;
    }
  }
  @media (max-width: 575px)
  {
    .techtitle
    {
      font-size:1.5em;
    }
    .tech2content
    {
      position:relative;
      width:100%;
      min-height:350px;
      padding-top:0px;
    }
    .techimages
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: center;
      margin-top: 50px;
    }
    .techcontent
    {
      margin-top:10px;
      padding:10px;
    }
    .techcontent img
    {
      width:70px;
      height:70px;
      border-radius: 15px;
    }
  }

</style>
