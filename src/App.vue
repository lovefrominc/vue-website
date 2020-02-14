<template>
  <div id="app">
    <div @click="change" id="menu-screen" v-bind:class="{top: top, opacity: opacity}">
      <router-link to="/">START</router-link>
      <router-link to="/investing">INVESTING</router-link>
      <router-link to="/jobs">JOBS</router-link>
      <router-link to="/about">ABOUT</router-link>
      <!-- <router-link to="/opensource">OPENSOURCE</router-link> -->
      <a href="https://github.com/lovefrominc" target="_blank">OPENSOURCE</a>
      <div id="close" @click="change">×</div>
    </div>
    <header id="nav">
      <div class="container std">
        <nav id="items">
                <div id="menu" @click="change">
                    <div class="lines"></div>
                    <div class="lines"></div>
                </div>

                <router-link to="/">
                  <div id="logo-name">
                      <div id="logo"></div>
                      <h1>LoveFrom</h1>
                  </div>
                </router-link>

                <div id="lg-links">
                  <!-- <router-link to="/">START</router-link> -->
                  <router-link to="/investing">INVESTING</router-link>
                  <router-link to="/jobs">JOBS</router-link>
                  <router-link to="/about">ABOUT</router-link>
                  <!-- <router-link to="/opensource">OPENSOURCE</router-link> -->
                  <a href="https://github.com/lovefrominc" target="_blank">OPENSOURCE</a>
                </div>
                <div id="info">
                    <div id="i">
                        
                    </div>
                </div>
        </nav>
      </div>
    </header>
    <router-view />
    <footer class="std container">
      <div id="footer-items">
        <div id="cpr">
          <p class="cpr">Copyright — All rights reserved</p>
          <p class="cpr">LoveFrom Inc. 2020</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<style>
@font-face {
  font-family: 'SF Pro Text';
  src: url("assets/fonts/SF-Pro-Text-Regular.ttf") format("font-truetype");
}
*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'SF Pro Text' !important;
}
.top{
  top: 0 !important;
}
.opacity{
  opacity: 1 !important;
}
body {
  background-color: #e8e8e8;
}
.container {
  padding: 0 34px 0 34px;
}
.std {
  padding-top: 38px;
  padding-bottom: 38px;
}
#items {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
#logo {
  width: 86px;
  height: 86px;
  border-radius: 24px;
  background-image: url("./assets/minimal-NO1.svg");
  background-size: 72px 72px;
  background-position: center;
  background-repeat: no-repeat;
  background-color: #e8e8e8;
  box-shadow: 2px 6px 16px rgba(135, 135, 135, 0.15),
    -4px -2px 16px rgba(255, 255, 255, 0.65);
}
#menu {
  width: 46px;
  height: 46px;
  display: flex;
  justify-content: space-between;
  flex-direction: column;
  padding-top: 14px;
  padding-bottom: 14px;
  padding-right: 7px;
  padding-left: 7px;
}
#menu .lines {
  width: 32px;
  height: 2px;
  background-color: #0d0d0d;
}
#info {
  width: 46px;
  height: 46px;
  padding: 6px;
}
#i {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  transform: scale(1.1);
  display: flex;
  justify-content: center;
  align-items: center;
  color: #0d0d0d;
  background-position: center;
  background-repeat: no-repeat;
}
#logo-name h1{
  display: none
}
#menu-screen {
  top:-100%;
  z-index: 1000;
  opacity: 0;
  transition: 0.2s ease-in-out;
  position: fixed;
  width: 100%;
  height: 100%;
  background-image: initial;
  background-color: rgba(135,135,135,0.80);
  backdrop-filter: blur(6px);
  -webkit-backdrop-filter: blur(6px);

  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-direction: column;
}
#menu-screen a {
  position: relative;
  z-index: 999;
  text-decoration: none;
  color: #fff;
}
#close{
    width: 68px;
    height: 68px;
    background-color: initial;
    color: #fff;
    font-size: 28px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 24px;
    box-shadow: 2px 6px 16px rgba(63, 63, 63, 0.25), -4px -2px 16px rgba(255,255,255,.25);
    cursor: pointer;
}
#lg-links{
  display: none;
}
.cpr{
    font-size: 16px;
    color: #7e7e7e;
    text-align: center;
}
#cpr{
    margin-top: 14px;
}
footer{
  margin-top: 34px;
  background-color: #0d0d0d;
}
.router-link-active{
  text-decoration: none !important;
}
.router-link-active #logo-name{
  color: #2a2a2a;
}
#logo::after{
  display: none;
}
@media screen and (min-width: 768px){
  .std{
    padding-top: 38px;
    padding-bottom: 38px;
  }
  .container{
    padding: 38px 10%;
  }
  #menu{
    display: none;
  }
  #logo-name{
    width: auto;
    display: flex;
    align-items: center;
  }
  #lg-links{
        display: block;
    }
    #lg-links a{
        text-decoration: none;
        color: #777777;
        margin-left: 18px;
        transition: all 0.2s;
    }
    #lg-links a:hover{
        color: #000;
    }
  #info{
    display: none;
  }
  #logo-name h1{
    display: block;
    margin-left: 18px;
    font-size: 32px;
  }
  #footer-items{
    display: flex;
    width: 100%;
    justify-content: center;
    
  }
  #logo::after{
    display: block;
    content: 'Home Page';
    width: 120px;
    position: relative;
    bottom: -150%;
    background-color: #2a2a2a;
    color: #fff;
    padding: 8px;
    border-radius: 6px;
    text-align: center;
    left: -17px;
    opacity: 0;
    transition: 0.6s all;
  }
  #logo:hover::after{
    bottom: -125%;
    opacity: 1;
  }
}
</style>

<script>
export default {
  data: () => {
    return {
      top: false,
      opacity: false
    }
  },
  methods: {
    change: function() {
      this.top = !this.top;
      this.opacity = !this.opacity;
    }
  }
};
</script>
