<script setup>
import {ref,onMounted} from 'vue'
let tabproject=ref(
[
    {id:0,thumb:'/projects/gamingshop_features/a.png',title:'Gaming Shop',link:"https://gamingshop-eta.vercel.app/",textalt:"Gaming thumb"},
    {id:1,thumb:'/projects/tictactoe_features/3.png',title:'Tic-Tac-Toe Game',link:"https://tictactoe-five-neon.vercel.app/",textalt:"Tic-tac-toe thumb"}
]);
let dialog=ref(false);

let weathertitle=ref("Weather App");
let housetitle=ref("House Showcase");
let gamingtitle=ref("Gaming Shop");
let tictactoetitle=ref("Tic-tac-toe Game");
let weatherlink=ref("https://weather.doriaarnaud.online/");
let houselink=ref("https://house.doriaarnaud.online/");
let gaminglink=ref("https://gamingshop.doriaarnaud.online/");
let tictactoelink=ref("https://tic-tac-toe.doriaarnaud.online/");
let weathertext=ref("A web application showing the daily weather in real time, auto-refreshing every defined delay with location, date, time features.")
let housetext=ref("A House Showcase Website example for exploring Apartments, Villas for rent, sale and a cta button. All the images are just examples and intentionally distorted but not a bugs.");
let gamingtext=ref("A gaming shop website example using Vue.js, Pinia, with search bar and cart management features. All the images are just examples and intentionally distorted but not a bugs.");
let tictactoetext=ref("A tic-tac-toe game using Vue.js with menu, loading progress and automatic re-drawing features.");

let weathertumbsrc=ref("/projects/weather_features/w1.png");
let housethumbsrc=ref("/projects/house_features/housethumb.jpg");
let gthumbsrc=ref("/projects/gamingshop_features/gthumb.jpg");
let tcthumbsrc=ref("/projects/tictactoe_features/tctthumb.jpg");
let weatherimages=ref([
  {images:'projects/weather_features/w1.png',textalt:'Weather features'},
  {images:'projects/weather_features/w1.png',textalt:'Weather features'},
  {images:'projects/weather_features/w1.png',textalt:'Weather features'},
  {images:'projects/weather_features/w1.png',textalt:'Weather features'}
])
let houseimages=ref([
  {images:'projects/house_features/img1.png',textalt:'House features'},
  {images:'projects/house_features/img2.png',textalt:'House features'},
  {images:'projects/house_features/img3.png',textalt:'House features'},
  {images:'projects/house_features/img4.png',textalt:'House features'}
])
let gamingimages=ref([
    {images:'/projects/gamingshop_features/a.png',textalt:"Gamingshop features"},
    {images:'/projects/gamingshop_features/b.png',textalt:"Gamingshop features"},
    {images:'/projects/gamingshop_features/c.png',textalt:"Gamingshop features"},
    {images:'/projects/gamingshop_features/d.png',textalt:"Gamingshop features"}
  ])
  let tocimages=ref([
    {images:'/projects/tictactoe_features/img1.png',textalt:"Tictactoe features"},
    {images:'/projects/tictactoe_features/img2.png',textalt:"Tictactoe features"},
    {images:'/projects/tictactoe_features/img3.png',textalt:"Tictactoe features"},
    {images:'/projects/tictactoe_features/img4.png',textalt:"Tictactoe features"},
    {images:'/projects/tictactoe_features/img5.png',textalt:"Tictactoe features"}
  ])
  let projtitle=ref();
  let projtext=ref();
  let projlink=ref();
  let houseslider=ref([]);
  let gslider=ref([]);
  let tcslider=ref([]);
  let mainslider=ref([]);
  let weathersrc=ref();
  let housesrc=ref();
  let gtsrc=ref();
  let tctsrc=ref();
  onMounted
  {
    weathersrc=weathertumbsrc.value;
    housesrc=housethumbsrc.value;
    gtsrc=gthumbsrc.value;
    tctsrc=tcthumbsrc.value;
    houseslider=houseimages.value;
    gslider=gamingimages.value;
    tcslider=tocimages.value;

  }
function changeslidersource(id)
{
  switch(id)
    {
      case 1:
       dialog.value=true;
       mainslider=houseimages;
       projtitle=housetitle.value;
       projtext=housetext.value;
       projlink=houselink.value;
       break;
      case 2:
        dialog.value=true;
        mainslider=gslider;
        projtitle=gamingtitle.value;
        projtext=gamingtext.value;
        projlink=gaminglink.value;
        break;
      case 3:
        dialog.value=true;
        mainslider=tcslider;
        projtitle=tictactoetitle.value;
        projtext=tictactoetext.value;
        projlink=tictactoelink.value;
        break;
    }
}

</script>
<template>
  <div class="featuredprojects">
      <v-card color="#09090d">
        <h1 class="featuredtitle ms-5 mt-5 h-auto">Featured Projects</h1>
        <div class="projs">
            <div class="houseproj ma-5 pa-5">
              <v-card color="#373b4f" class="houseprojthumb mt-5">
                <v-img :src="housesrc"
                       title="See project features"
                       alt="house image thumbs"
                       @click="changeslidersource(1)">
                </v-img>
              </v-card>
              <p class="text-h6 mt-4 mb-4" id="ptitle">House Showcase</p>
               <v-btn color="#ffffff" href="https://house.doriaarnaud.online/" target="blank">
                 Visit project
               </v-btn>
               <v-btn class="detailsbtn mt-5" color="#b90000" @click="changeslidersource(1)">
                 See details...
               </v-btn>
            </div>

            <div class="gamingproj ma-5 pa-5">
              <v-card color="#373b4f" class="gamingprojthumb mt-5">
                <v-img :src="gtsrc"
                       title="See project features"
                       alt="gaming shop thumb"
                       @click="changeslidersource(2)">
                </v-img>
              </v-card>
              <p class="text-h6 mt-4 mb-4" id="ptitle">Gaming shop</p>
               <v-btn color="#ffffff" href="https://gamingshop.doriaarnaud.online/" target="blank">
                 Visit project
               </v-btn>
               <v-btn class="detailsbtn mt-5" color="#b90000" @click="changeslidersource(2)">
                 See details...
               </v-btn>
            </div>

            <div class="ticproj ma-5 pa-5">
              <v-card color="#373b4f" class="ticprojthumb mt-5">
                <v-img :src="tctsrc"
                          title="See project features"
                          alt="tic-tac-toe thumb"
                          @click="changeslidersource(3)">
                </v-img>
              </v-card>


              <p class="text-h6 mt-4 mb-4" id="ptitle">Tic-Tac-Toe game</p>
              <v-btn color="#ffffff" href="https://tic-tac-toe.doriaarnaud.online/" target="blank">
                Visit project
              </v-btn>
              <v-btn class="detailsbtn mt-5" color="#b90000" @click="changeslidersource(3)">
                See details...
              </v-btn>
            </div>
        </div>
      </v-card>
  </div>
  <div class="carousselcontainer text-center pa-4">
    <v-dialog
          v-model="dialog"
          transition="dialog-bottom-transition"
          fullscreen
        >
      <v-card>
        <v-toolbar>
          <v-btn
            icon="mdi-close"
            @click="dialog = false"
          ></v-btn>

        </v-toolbar>
        <div class="carousselcontainer">
          <div class="carousselcontent mt-5">
            <v-carousel
                  cycle
                  height="400"
                  hide-delimiter-background
                  show-arrows="hover">
                <v-carousel-item
                  v-for="techimg in mainslider" :key="techimg.id"
                >
                 <img :src="techimg.images" :alt="techimg.textalt" id="carousselitems">

                 </img>
                </v-carousel-item>
            </v-carousel>
                <v-card class="mt-1 ms-1 mr-1" :title="projtitle" :text="projtext">

                </v-card>
                <v-btn color="#004200" class="ms-1 mt-5"
                        :href="projlink"
                        target="blank"
                        :title="projlink">
                  Visit project
                </v-btn>
          </div>
        </div>
      </v-card>
    </v-dialog>
</div>
</template>

<script>
</script>

<style>
  @media (min-width: 1200px)
  {
    .carousselcontent
    {
      width:950px;
      margin-left:auto;
      margin-right:auto;
    }
    img#carousselitems
    {
      border:2px solid #a0a0a0;
      border-radius: 5px;
      width:550px;
      display:block;
      margin-left:auto;
      margin-right:auto;
    }
    .featuredprojects
    {
      min-height: 400px;
      margin-top:50px;
      margin-left:auto;
      margin-right:auto;
    }
    .featuredprojects .houseprojthumb
    {
        width:300px;
        height:200px;
    }
    .houseproj button
    {
      display:block;
    }
    .featuredprojects .gamingprojthumb
    {
        width:300px;
        height:200px;
    }
    .gamingproj button
    {
      display:block;
    }
    .featuredprojects .ticprojthumb
    {
        width:300px;
        height:200px;
    }
    .ticproj button
    {
      display:block;
    }
    .projs
    {
      display:flex;
      justify-content: center;
      flex-wrap: wrap;
      margin-top: 50px;
    }
    .projs img:hover
    {
      cursor: pointer;
    }
  }
  @media (min-width: 992px) and (max-width: 1199px)
  {
    .carousselcontent
    {
      width:950px;
      margin-left:auto;
      margin-right:auto;
    }
    img#carousselitems
    {
      border:2px solid #a0a0a0;
      border-radius: 5px;
      width:550px;
      display:block;
      margin-left:auto;
      margin-right:auto;
    }
    .featuredprojects
    {
      min-height: 400px;
      margin-top:50px;
    }
    .featuredprojects .houseproj
    {
        width:300px;
        border-radius: 10px;
    }
    .featuredprojects .gamingproj
    {
        width:300px;
        border-radius: 10px;
    }
    .featuredprojects .ticproj
    {
        width:300px;
        border-radius: 10px;
    }
    .projs
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      margin-top: 50px;
    }
    .houseproj button
    {
      display:block;
    }
    .gamingproj button
    {
      display:block;
    }
    .ticproj button
    {
      display:block;
    }
    .projs img:hover
    {
      cursor: pointer;
    }
  }
  @media (min-width: 768px) and (max-width: 991px)
  {
    .carousselcontent
    {
      width:650px;
      margin-left:auto;
      margin-right:auto;
    }
    img#carousselitems
    {
      border:2px solid #a0a0a0;
      border-radius: 5px;
      width:550px;
      display:block;
      margin-left:auto;
      margin-right:auto;
    }
    .featuredprojects
    {
      min-height: 400px;
      margin-top:50px;
    }
    .featuredprojects .houseproj
    {
        width:300px;
        border-radius: 10px;
    }
    .featuredprojects .gamingproj
    {
        width:300px;
        border-radius: 10px;
    }
    .featuredprojects .ticproj
    {
        width:300px;
        border-radius: 10px;
    }
    .projs
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: center;
      margin-top: 50px;
    }

    .projs img:hover
    {
      cursor: pointer;
    }
  }
  @media (min-width: 576px) and (max-width: 767px)
  {
    .featuredtitle
    {
      font-size:1.5em;
    }
    .carousselcontent
    {
      width:550px;
      margin-left:auto;
      margin-right:auto;
    }
    img#carousselitems
    {
      border:2px solid #a0a0a0;
      border-radius: 5px;
      width:550px;
      display:block;
      margin-left:auto;
      margin-right:auto;
    }
    .featuredprojects
    {
      min-height: 400px;
      margin-top:50px;
    }
    button.detailsbtn
    {
      display:none;
    }
    .featuredprojects .houseproj
    {
        width:80%;
        border-radius: 10px;
    }
    .featuredprojects .gamingproj
    {
        width:80%;
        border-radius: 10px;
    }
    .featuredprojects .ticproj
    {
        width:80%;
        border-radius: 10px;
    }
    .projs
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: center;
      margin-top: 50px;
    }
  }
  @media (max-width: 575px)
  {
    .featuredtitle
    {
      font-size:1.5em;
    }
    .carousselcontent
    {
      width:100%;
      margin-left:auto;
      margin-right:auto;
    }
    img#carousselitems
    {
      border:2px solid #a0a0a0;
      border-radius: 5px;
      width:100%;
      display:block;
      margin-left:auto;
      margin-right:auto;
    }
    .featuredprojects
    {
      min-height: 400px;
      margin-top:50px;
    }
    button.detailsbtn
    {
      display:none;
    }
    .featuredprojects .houseproj
    {
        width:100%;
        border-radius: 10px;
    }
    .featuredprojects .gamingproj
    {
        width:100%;
        border-radius: 10px;
    }
    .featuredprojects .ticproj
    {
        width:100%;
        border-radius: 10px;
    }
    .projs
    {
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: center;
      margin-top: 50px;
    }
  }
</style>
