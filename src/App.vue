<template>
  <v-app id="app">
  <body :class="{ modalActive: isActive}">
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

    <v-container  style="margin-top:80px;">

<div id="modal-container" :class="{six : isActive}">
  <div class="modal-background">
    <div class="modal">
      <h2>Pour ma léa</h2>
      <p>Hear me roar.</p>
      <svg class="modal-svg" xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" preserveAspectRatio="none">
            <rect x="0" y="0" fill="none" width="226" height="162" rx="3" ry="3"></rect>
            </svg>
    </div>
  </div>
</div>

      <div class="grid">
      <div
      @click="isActive= true"
      v-for="box in boxes" :key="box.id" class="item"
      :class="box.item"
      :style="{ 'background-image': 'url(' + box.style + ')' }">
      </div>
      <!--
        <div
        @click="isActive= true"
          class="item item--large"
          :style="{ 'background-image': 'url(' + couvPoucet + ')' }"
        >
        </div>

    <div class="item item--large " :style="{ 'background-image': 'url(' + illu1 + ')' }">
    </div>

      <div class="item item--large " :style="{ 'background-image': 'url(' + illu2 + ')' }">
    </div>

    <div class="item item--large " :style="{ 'background-image': 'url(' + illu3 + ')' }">
    </div>
    <div class="item item--hori" :style="{ 'background-image': 'url(' + cabochon3 + ')' }">
    </div>
    <div class="item item--large " :style="{ 'background-image': 'url(' + cabochon1 + ')' }">
    </div>

      <div class="item item--long " :style="{ 'background-image': 'url(' + coureMir + ')' }">
    </div>
      <div class="item item--long " :style="{ 'background-image': 'url(' + femme + ')' }">
    </div>
      <div class="item item--long " :style="{ 'background-image': 'url(' + frere + ')' }">
    </div>
    <div class="item item--full " :style="{ 'background-image': 'url(' + enterrement + ')' }">
    </div> -->
</div>

      </v-container>

    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
 </body>
  </v-app>
</template>

<script>

import couvPoucet from '../src/assets/img/illu/couv.jpg'
import cabochon1 from '../src/assets/img/illu/cabochon1.png'
import cabochon3 from '../src/assets/img/illu/cabochon3.png'
import illu1 from '../src/assets/img/illu/illu1.jpg'
import illu2 from '../src/assets/img/illu/illu2.jpg'
import illu3 from '../src/assets/img/illu/illu3_compressed.jpg'

import image from '../src/assets/img/pirate/couv_contraire.jpg'
import foireTen from '../src/assets/img/inde/foire_tenebres.jpg'
import coureMir from '../src/assets/img/inde/cour_miracles.jpg'
import femme from '../src/assets/img/croquis/femme.jpg'
import frere from '../src/assets/img/croquis/frere2.jpg'
import carpe from '../src/assets/img/croquis/jap.jpg'
import enterrement from '../src/assets/img/enterrement.jpg'

export default {

  name: 'app',

  data () {
    return {
      bodyAtc: false,
      isActive: false,
      image: image,
      couvPoucet: couvPoucet,
      foireTen: foireTen,
      femme: femme,
      frere: frere,
      coureMir: coureMir,
      carpe: carpe,
      enterrement: enterrement,
      cabochon1: cabochon1,
      cabochon3: cabochon3,
      illu1: illu1,
      illu2: illu2,
      illu3: illu3,
      boxes: [
        {
          item: 'item--large',
          style: illu1
        },
        {
          item: 'item--large',
          style: illu2
        },
        {
          item: 'item--large',
          style: illu3
        },
        {
          item: 'item--hori',
          style: cabochon3
        },
        {
          item: 'item--large',
          style: cabochon1
        },
        {
          item: 'item--long',
          style: coureMir
        },
        {
          item: 'item--long',
          style: femme
        }
      ]
    }
  },

  components: {

  }
}
</script>

<style lang="scss">
</style>
