<template>
  <div id="app">
  <div style="background: #fafafa">
   <header class="header align-bottom" style="height:200px;padding-top:70px;">

   <v-layout column align-center  justify-center fill-height style="padding-bottom:50px;">
        <v-img alt="Vue logo"  width="170px" :src="require('../src/assets/img/inde/logo_illu.png')"/>
      </v-layout>

      <div class="mobile-menu-trigger">
    <span class="ex"></span>
</div>
<nav class="menu" style="top: 200px;">
    <ul>

                <li class=" selected">
                    <a href="/branding">ILLUSTRATION</a>
                </li>

                <li class="">
                    <a href="/4340512-illustration">GRAPHISME</a>
                </li>

                <li class="">
                    <a href="/about">ABOUT &amp; CONTACT</a>
                </li>

    </ul>
</nav>

</header>
</div>
    <v-container pt-5>

  <!--
      <v-layout column align-center justify-center row fill-height >
        <v-img alt="Vue logo" fluid width="250px" :src="require('../src/assets/img/inde/logo_illu.png')"/>
      </v-layout>-->

    <!--<v-row class="justify-content-md-center">
        <v-col cols="12" md="auto">Graphisme</v-col>
        <v-col cols="12" md="auto">Illustration</v-col>
        <v-col cols="12" md="auto">A propos</v-col>
        <v-col cols="12" md="auto">Contact</v-col>
    </v-row>-->

      <v-container class="bv-example-row" style="padding-left:auto;padding-right:auto;">

      <div class="rowImg">
      <div
      v-for="item in items"
      :key="item.id"
      class="columnImg">
      <img  style="width:100%"
        :src="item.style">
    </div>

</div>

      </v-container>

    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
    </v-container>
  </div>
</template>

<script>

import image from '../src/assets/img/pirate/couv_contraire.jpg'
import couvPoucet from '../src/assets/img/illu/couv.jpg'
import foireTen from '../src/assets/img/inde/foire_tenebres.jpg'
import coureMir from '../src/assets/img/inde/cour_miracles.jpg'
import femme from '../src/assets/img/croquis/femme.jpg'
import frere from '../src/assets/img/croquis/frere2.jpg'

export default {

  name: 'app',

  data () {
    return {
      items: [
        {
          index: 1,
          style: couvPoucet
        },
        {
          index: 2,
          style: image
        },
        {
          index: 3,
          style: foireTen
        },
        {
          index: 4,
          style: coureMir
        },
        {
          index: 5,
          style: femme
        },
        {
          index: 6,
          style: frere
        },
        {
          index: 7,
          style: couvPoucet
        }
      ]
    }
  },

  components: {

  }
}
</script>

<style lang="scss">
.header{
  background: #fafafa;

}
.header.align-bottom .menu {
    background: #fafafa;
    padding: 16px;
    position: absolute;
}
.header.align-bottom {
    background: #fafafa;
}
.header.align-top, .header.align-bottom {
    padding-top: 0px;
    text-align: center;
}
.menu ul {
    list-style: none;
    margin: 0 auto;
}
.menu li {
    display: inline-block;
    margin: 0 25px 16px 25px;
}
.menu li.selected > a {
    color: #ed8374;
    font-weight: normal;
    text-decoration: none;
}
.menu li > a {
    color: #222222;
    font-family: lato, sans-serif;
    font-size: 15px;
    text-decoration: none;
}
a {
    outline: none;
    color: #444444;
    font-style: normal;
    font-weight: normal;
    text-decoration: underline;
}
.menu {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    z-index: 98;
}
/*
*
*
*
*/
.rowImg {
  display: -ms-flexbox; /* IE10 */
  display: flex;
  -ms-flex-wrap: wrap; /* IE10 */
  flex-wrap: wrap;
  padding: 0 4px;
}

/* Create four equal columnImgs that sits next to each other */
.columnImg {
  -ms-flex: 25%; /* IE10 */
  flex: 25%;
  max-width: 25%;
  padding: 0 4px;
}

.columnImg img {
  margin-top: 8px;
  vertical-align: middle;
}

/* Responsive layout - makes a two column-layout instead of four columns */
@media screen and (max-width: 800px) {
  .columnImg {
    -ms-flex: 50%;
    flex: 50%;
    max-width: 50%;
  }
}

/* Responsive layout - makes the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .columnImg {
    -ms-flex: 100%;
    flex: 100%;
    max-width: 100%;
  }
}

/*
*
*
*
*/
.item {
  position: absolute;
  top: 5px;
  left: 5px;
  right: 5px;
  bottom: 5px;
  font-size: 1.2em;
  color: rgb(0,158,107);
}
.item:after {
  content: attr(index);
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
</style>
