<script setup>
import {ref} from 'vue'
let userinputloaded=ref(false);
let userinputnotloaded=ref(true);
let userinput=ref();
function enablecontact()
{
  if(userinput.value==5)
  {
    userinput.value='';
    setTimeout(()=>
    {
      userinputnotloaded.value=false;
      userinputloaded.value=true;
    },500);
  }
  else
  {
    userinputnotloaded.value=true;
    userinputloaded.value=false;
    userinput.value='';
  }
}
function inputreset()
{
  userinputnotloaded.value=true;
  userinputloaded.value=false;
  userinput.value='';
}
</script>
<template>
  <div class="contactcontainer">
    <div class="contactcontent">
        <h1 class="text-h4 mt-16 ms-8">
          Let's work together on Your next project
        </h1>
        <h3 class="text-subtitle-1 ms-8">
          If you have an idea, my contact is great open.
        </h3>
        <div class="verif ms-8 mt-5">
          <p class="text-h6">2 + 3 = ?</p>
          <input type="number" name="verification" class="inputverif ps-2" v-model="userinput" placeholder="Please type the result..."/>
          <v-btn class="ms-5" @click="enablecontact">
            OK
          </v-btn>
        </div>
        <v-btn color="#b90000" class="ms-8 mb-8 mt-8" size="large" v-if="userinputnotloaded" disabled>
          Contact
        </v-btn>
        <v-btn color="#b90000" class="ms-8 mb-8 mt-8" size="large" v-if="userinputloaded" @click="inputreset"
        href="mailto:online.doriaarnaud@gmail.com" target="blank">
            Contact
        </v-btn>
    </div>
  </div>
</template>

<script>
</script>

<style>
  @media (min-width: 1200px)
  {
    .contactcontainer
    {
      margin-top:50px;
    }
    .contactcontent
    {
      width:950px;
      margin-left:auto;
      margin-right:auto;
      border:1px solid #9f9f9f;
      min-height: 200px;
      background-color:#000000;
      border-radius:10px;
      color:#ffffff;
    }
    input.inputverif
    {
      background-color: #ffffff;
      border-radius: 5px;
      width:40%;
      height:37px;
    }
  }
  @media (min-width: 992px) and (max-width: 1199px)
  {
    .contactcontainer
    {
      margin-top:50px;
    }
    .contactcontent
    {
      width:800px;
      margin-left:auto;
      margin-right:auto;
      border:1px solid #9f9f9f;
      min-height: 200px;
      background-color:#000000;
      border-radius:10px;
      color:#ffffff;
    }
    input.inputverif
    {
      background-color: #ffffff;
      border-radius: 5px;
      width:50%;
      height:37px;
    }
  }
  @media (min-width: 768px) and (max-width: 991px)
  {
    .contactcontainer
    {
      margin-top:50px;
    }
    .contactcontent
    {
      width:700px;
      margin-left:auto;
      margin-right:auto;
      border:1px solid #9f9f9f;
      min-height: 200px;
      background-color:#000000;
      border-radius:10px;
      color:#ffffff;
    }
    input.inputverif
    {
      background-color: #ffffff;
      border-radius: 5px;
      width:50%;
      height:37px;
    }
  }
  @media (min-width: 576px) and (max-width: 767px)
  {
    .contactcontainer
    {
      margin-top:50px;
    }
    .contactcontent
    {
      width:550px;
      margin-left:auto;
      margin-right:auto;
      border:1px solid #9f9f9f;
      min-height: 200px;
      background-color:#000000;
      border-radius:10px;
      color:#ffffff;
    }
    input.inputverif
    {
      background-color: #ffffff;
      border-radius: 5px;
      width:50%;
      height:37px;
    }
  }
  @media (max-width: 575px)
  {
    .contactcontainer
    {
      margin-top:50px;
    }
    .contactcontent
    {
      width:100%;
      margin-left:auto;
      margin-right:auto;
      border:1px solid #9f9f9f;
      min-height: 200px;
      background-color:#000000;
      border-radius:10px;
      color:#ffffff;
    }
    input.inputverif
    {
      background-color: #ffffff;
      border-radius: 5px;
      width:50%;
      height:40px;
    }
  }
</style>
