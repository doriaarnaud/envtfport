<script setup>
import {ref,onMounted} from 'vue'
import Presentation from '@/components/Presentation.vue'
import About from '@/components/About.vue'
import Projects from '@/components/Projects.vue'
import Technologies from '@/components/Technologies.vue'
import Contact from '@/components/Contact.vue'
import Privacy from '@/components/Privacy.vue'
function scroll(refName)
{
  const element=document.getElementById(refName);
  element.scrollIntoView({ behavior: "smooth"});
}
</script>
<template>
  <v-app-bar class="navigationbar" color="#000000">
    <v-spacer></v-spacer>
    <v-btn
       class="btnav text-h6" @click="scroll('presentation')">Home</v-btn>
    <v-btn
       class="btnav text-h6" @click="scroll('about')">About</v-btn>
    <v-btn
       class="btnav text-h6" @click="scroll('featuredproject')">Projects</v-btn>
    <v-btn
       class="btnav text-h6" @click="scroll('contact')">Contact</v-btn>
  </v-app-bar>
    <div id="presentationcontainer">
      <v-container id="presentation">
        <Presentation >


        </Presentation>
      </v-container>
    </div>
    <div id="aboutcontainer">
      <v-container id="about">
        <About >

        </About>
      </v-container>
    </div>
    <div id="featuredcontainer">
      <v-container id="featuredproject">
        <Projects >

        </Projects>
        <Technologies>

        </Technologies>
      </v-container>
    </div>
    <div id="contactcontainer">
      <v-container id="contact" >
        <Contact >

        </Contact>
      </v-container>
      <v-container>
        <Privacy>

        </Privacy>
      </v-container>
    </div>
</template>



<script>
  export default
  {
  data: () => ({

      })
  }
</script>
<style>
  @media (min-width: 1200px)
  {
    #presentationcontainer
    {
      background-color:#101019;
      color:#ffffff;
    }
    #aboutcontainer
    {
      background-color:#09090d;
    }
    #featuredcontainer
    {
      background-color:#09090d;
    }
    #contactcontainer
    {
      background-color:#101019;
    }
    .btnav
    {
      background-color: #000000;
      color:#ffffff;
      text-decoration:underline;
    }
  }
  @media (min-width: 992px) and (max-width: 1199px)
  {
    #presentationcontainer
    {
      background-color:#101019;
      color:#ffffff;
    }
    #aboutcontainer
    {
      background-color:#09090d;
    }
    #featuredcontainer
    {
      background-color:#09090d;
    }
    #contactcontainer
    {
      background-color:#101019;
    }
    .btnav
    {
      background-color: #000000;
      color:#ffffff;
      text-decoration:underline;
    }
  }
  @media (min-width: 768px) and (max-width: 991px)
  {
   #presentationcontainer
   {
     background-color:#101019;
     color:#ffffff;
   }
   #aboutcontainer
   {
     background-color:#09090d;
   }
   #featuredcontainer
   {
     background-color:#09090d;
   }
   #contactcontainer
   {
     background-color:#101019;
   }
    .btnav
    {
      background-color: #000000;
      color:#ffffff;
      text-decoration:underline;
    }
  }
  @media (min-width: 576px) and (max-width: 767px)
  {
    #presentationcontainer
    {
      background-color:#101019;
      color:#ffffff;
    }
    #aboutcontainer
    {
      background-color:#09090d;
    }
    #featuredcontainer
    {
      background-color:#09090d;
    }
    #contactcontainer
    {
      background-color:#101019;
    }
    .btnav
    {
      background-color: #000000;
      color:#ffffff;
      text-decoration:underline;
    }
  }
  @media (max-width: 575px)
  {
    #presentationcontainer
    {
      background-color:#101019;
      color:#ffffff;
    }
    #aboutcontainer
    {
      background-color:#09090d;
    }
    #featuredcontainer
    {
      background-color:#09090d;
    }
    #contactcontainer
    {
      background-color:#101019;
    }
    .btnav
    {
      background-color: #000000;
      color:#ffffff;
      width:90px;
      text-decoration:underline;
    }
  }
</style>
