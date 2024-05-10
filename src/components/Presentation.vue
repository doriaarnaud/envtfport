<script setup>

</script>
<template>
  <div class="presentation h-auto">
    <div class="presentationcontent">
      <div class="avatar">
        <img src="/profile/Me.jpg" alt="Doria Arnaud image" title="Doria Arnaud image"/>
      </div>
       <div class="presentationtext">
           <h1 class="hello mt-8">Hello, I'm</h1>
           <h1 class="firstname mt-2">Doria Arnaud</h1>
           <h1 class="myact mt-2">Front-end Web Developer</h1>
       </div>
     </div>
  </div>
</template>

<script>
</script>

<style>
  @media (min-width: 1200px)
  {
    .presentation
    {
      min-height:400px;
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 150px;
    }
    .presentationcontent
    {
      width:950px;
      margin-left:auto;
      margin-right:auto;
    }
    .presentationcontent .avatar
    {
      float:left;
    }
    .presentationcontent .avatar img
    {
        border-radius: 120px 120px 0px 120px;
        border:2px solid #a0a0a0;
    }
    .presentationcontent .presentationtext
    {
      margin-top: 20px;
      float:right;
    }
    h1.hello,h1.firstname
    {
      font-size:2.5em;
    }
    h1.myact
    {
      font-size:1em;
    }
  }
  @media (min-width: 992px) and (max-width: 1199px)
  {
    .presentation
    {
      min-height:400px;
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 150px;
    }
    .presentationcontent
    {
      width:950px;
      margin-left:auto;
      margin-right:auto;
    }
    .presentationcontent .avatar
    {
      float:left;
    }
    .presentationcontent .avatar img
    {
        border-radius: 120px 120px 0px 120px;
        border:2px solid #a0a0a0;
    }
    .presentationcontent .presentationtext
    {
      margin-top: 20px;
      float:right;
    }
    h1.hello,h1.firstname
    {
      font-size:2.5em;
    }
    h1.myact
    {
      font-size:1em;
    }
  }
  @media (min-width: 768px) and (max-width: 991px)
  {
    .presentation
    {
      min-height:400px;
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 150px;
    }
    .presentationcontent
    {
      width:950px;
      margin-left:auto;
      margin-right:auto;
    }
    .presentationcontent .avatar
    {
      float:left;
      padding-left:20px;
    }
    .presentationcontent .avatar img
    {
        border-radius: 120px 120px 0px 120px;
        border:2px solid #a0a0a0;
    }
    .presentationcontent .presentationtext
    {
      margin-top: 20px;
      float:right;
      padding-right:20px;
    }
    h1.hello,h1.firstname
    {
      font-size:2.5em;
    }
    h1.myact
    {
      font-size:1em;
    }
  }
  @media (min-width: 576px) and (max-width: 767px)
  {
    .presentation
    {
      min-height:400px;
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 150px;
    }
    .presentationcontent .avatar img
    {
        border-radius: 120px 120px 0px 120px;
        border:2px solid #a0a0a0;
        display:block;
        width:250px;
        height:250px;
    }
    h1.hello,h1.firstname
    {
      font-size:2.2em;
    }
    h1.myact
    {
      font-size:1em;
    }
  }
  @media (max-width: 575px)
  {
    .presentation
    {
      min-height:400px;
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 100px;
    }
    .presentationcontent .avatar img
    {
        border-radius: 120px 120px 0px 120px;
        border:2px solid #a0a0a0;
        display:block;
        width:200px;
        height:200px;
    }
    h1.hello,h1.firstname
    {
      font-size:2em;
    }
    h1.myact
    {
      font-size:0.9em;
    }
  }
</style>
