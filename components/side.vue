<template>
  <div class ="container">
    <head><link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet"> </head>
    <body>
  <section class="side">
    <img src = "../assets/img/Logo.svg" class = "logo">
    <div id="nav-drawer">
      <input id="nav-input" type="checkbox" class="nav-unshown">
      <label for="nav-input"><span></span></label>
      <label class="nav-unshown" id="nav-close" for="nav-input"></label>
      <div id="nav-content">
        <h1><nuxt-link to="/">WORKS</nuxt-link></h1>
        <h1><nuxt-link to="/about">ABOUT</nuxt-link></h1>
        <div class = "border_v"></div>
        <a href="https://twitter.com/mt_book10" target="_blank" class="animsition-link"><h2 class="h2-t">Twitter</h2></a>
        <a href="https://www.facebook.com/YMMT.SUM" target="_blank" class="animsition-link"><h2 class="h2-f">Facebook</h2></a>
        <a href="https://dribbble.com/mt_book10" target="_blank" class="animsition-link"><h2 class="h2-d">Dribbble</h2></a>
      </div>
  </div>
    <h1><nuxt-link to="/">WORKS</nuxt-link></h1>
    <h1><nuxt-link to="/about">ABOUT</nuxt-link></h1>
    <div class = "border_v"></div>
    <a href="" target="_blank" class="animsition-link"><h2 class="h2-t">Twitter</h2></a>
    <a href="" target="_blank" class="animsition-link"><h2 class="h2-f">Facebook</h2></a>
    <a href="https://dribbble.com/mt_book10" target="_blank" class="animsition-link"><h2 class="h2-d">Dribbble</h2></a>
  </section>
  </body>
  </div>
</template>

<style scoped>
html{
  color: #272727;
}

@media screen and (max-width: 1023px) {

.logo{
  position: fixed;
  width: 20vw;
  min-width: 150px;
  text-align: center;
  margin: 1.5rem;
  }

  #nav-content{
    padding-top: 3rem;
  }

  .side #nav-content h1{
  display: block !important;
  width: auto;
  margin: 1rem 0 0 3rem;
  font-family: 'Cormorant Garamond', serif;
  font-weight: 400;
  font-style: italic;
  transition: .5s;
  letter-spacing: 0.3rem;
}
.side #nav-content h1:hover{
  width: auto;
  font-family: 'Cormorant Garamond', serif;
  font-weight: 700;
  font-style: normal;
}
.side #nav-content a{
  text-decoration: none !important;
  color: #272727;
}
.side #nav-content h2{
  display: block !important;
  margin: 2.5rem 0 0 3rem;
  line-height: 0;
  font-family: 'Cormorant Garamond', serif;
  font-weight: 400;
  font-style: italic;
  font-size: 1.2rem;
  transition: .5s;
}
.side #nav-content h2:hover{
  width: auto;
  font-family: 'Cormorant Garamond', serif;
  font-weight: 700;
  font-style: normal;
}

.side h1 , .side h2{
    display: none;
  }

.h2-t:hover{
  color: #1da1f2 !important;
}
.h2-f:hover{
  color: #4064ac !important;
}
.h2-d:hover{
  color: #ea4c89 !important;
}

  label {
  display: block;
  position: fixed;
  top: 2.5rem;
  right: 2.5rem;
  width: 30px;
  height: 20px;
  background: none;
  border: none;
  cursor: pointer;
  outline: none;
}
label span {
  width: 100%;
  height: 2px;
  background: #000;
  display: block;
  margin: 0;
  border-radius: 100px;
  position: relative;
  left: -10px;
  transition: 0.2s cubic-bezier(1, 0.3, 0, 0.3);
}
label span::before {
  content: "";
  width: 100%;
  height: 2px;
  background: #000;
  display: block;
  position: absolute;
  top: -200%;
  border-radius: 100px;
  left: 10px;
  transition: 0.2s cubic-bezier(1, 0.3, 0, 0.3);
}
label span::after {
  content: "";
  width: 100%;
  height: 2px;
  background: #000;
  display: block;
  position: absolute;
  bottom: -200%;
  border-radius: 100px;
  right: -5px;
  transition: 0.2s cubic-bezier(1, 0.3, 0, 0.3);
}

label:hover span {
  left: 5px;
  transition: 0.4s cubic-bezier(1, 0.3, 0, 0.3);
}
label:hover span::before {
  left: 0;
  transition: 0.4s cubic-bezier(1, 0.3, 0, 0.3);
}
label:hover span::after {
  right: 0;
  transition: 0.4s cubic-bezier(1, 0.3, 0, 0.3);
}

.label-toggled span {
  left: 5px;
  background: transparent;
  top: 5px;
  transition: 0.3s cubic-bezier(1, 0.3, 0, 0.3) !important;
}
.label-toggled span::before {
  left: 0;
  transform-origin: center-left;
  transform: rotate(-45deg);
  bottom: 5px;
  transition: 0.3s cubic-bezier(1, 0.3, 0, 0.3) !important;
}
.label-toggled span::after {
  right: 0;
  transform-origin: center-right;
  transform: rotate(45deg);
  top: -5px;
  transition: 0.3s cubic-bezier(1, 0.3, 0, 0.3) !important;
}

.label-toggled:hover span {
  left: 5px;
}
.label-toggled:hover span::before {
  left: 0;
}
.label-toggled:hover span::after {
  left: 0;
}

#nav-drawer {
  position: relative;
}

/*チェックボックス等は非表示に*/
.nav-unshown {
  display:none;
}

/*閉じる用の薄黒カバー*/
#nav-close {
  display: none;/*はじめは隠しておく*/
  position: fixed;
  z-index: 9998;
  top: 0;/*全体に広がるように*/
  left: 0;
  width: 100%;
  height: 100%;
  background: black;
  opacity: 0;
  transition: .5s ease-in-out;
}

/*中身*/
#nav-content {
  overflow: auto;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 9999;/*最前面に*/
  width: 90%;/*右側に隙間を作る（閉じるカバーを表示）*/
  max-width: 330px;/*最大幅（調整してください）*/
  height: 100%;
  background: #fff;/*背景色*/
  transition: .5s ease-in-out;/*滑らかに表示*/
  -webkit-transform: translateX(-105%);
  transform: translateX(-105%);/*左に隠しておく*/
}

/*チェックが入ったらもろもろ表示*/
#nav-input:checked ~ #nav-close {
  display: block;/*カバーを表示*/
  opacity: .5;
}

#nav-input:checked ~ #nav-content {
  -webkit-transform: translateX(0%);
  transform: translateX(0%);/*中身を表示（右へスライド）*/
  box-shadow: 6px 0 25px rgba(0,0,0,.15);
}

}

@media screen and (min-width: 1024px) {

.logo{
   width: 12vw;
   text-align: center;
   margin: 3rem 0 2rem 3vw;
 }
#nav-drawer{
  display: none;
}
.side {
  height: 100vh;
  width: 25vw;
}
.side h1{
  width: auto;
  margin: 3rem 0 3rem 3vw;
  font-family: 'Cormorant Garamond', serif;
  font-weight: 400;
  font-style: italic;
  transition: .5s;
  letter-spacing: 0.3rem;
}
.side h1:hover{
  width: auto;
  font-family: 'Cormorant Garamond', serif;
  font-weight: 700;
  font-style: normal;
}
.side a{
  text-decoration: none !important;
  color: #272727;
}
.side h2{
  margin: 3rem 0 3rem 3vw;
  line-height: 0;
  font-family: 'Cormorant Garamond', serif;
  font-weight: 400;
  font-style: italic;
  font-size: 1.2rem;
  transition: .5s;
}
.side h2:hover{
  width: auto;
  font-family: 'Cormorant Garamond', serif;
  font-weight: 700;
  font-style: normal;
}
.side label{
  display: none;
}
.h2-t:hover{
  color: #1da1f2 !important;
}
.h2-f:hover{
  color: #4064ac !important;
}
.h2-d:hover{
  color: #ea4c89 !important;
}
.side {
  padding: 2%;
}
.border_v{
  display: block;
  width: 0.8px;
  background-color: #272727;
  height: 25vh;
  margin: 0 0 0 4vw;
}
 
}

</style>
