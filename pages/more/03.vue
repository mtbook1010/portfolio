<template>
<div class ="container">
    <head>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,700;1,400&family=Noto+Serif+JP:wght@200;600&display=swap" rel="stylesheet">
    </head>
    <body class="animsition">
    <div id="side">
      <Side />
    </div>
  <h1 class="main_t">#ym2t</h1>
  <div class="main">
    <section>
    <img src="~/assets/img/03-min.png">
    <p><a href="https://ym2t.netlify.app/" target="_blank"><span>></span> https://ym2t.netlify.app/</a></p>
    </section>
    <section>
    <img src="~/assets/img/more-img/03-m-00-min.png">
    </section>
    <section>
    <img src="~/assets/img/more-img/03-m-01-min.png">
    </section>
    <section>
    <img src="~/assets/img/more-img/03-m-02-min.png">
    </section>
    </div>
  </body>
</div>
</template>

<script>
export default {
  components: {
    Side: () => import('~/components/side')
  }
}
</script>>

<style scoped>

body{
  background: #f8f8f8 !important;
  color: #272727;
}

@media screen and (max-width: 1023px) {

#side{
  position: fixed;
  z-index: 9999;
}
.main_t{
  position: fixed;
  top: 4rem;
  right: 5vw;
  margin: 0;
  font-family: 'Cormorant Garamond', serif;
  font-weight: 700;
  font-size: 5rem;
  color: #dadada;
  letter-spacing: 0.5rem;
}
.main{
  display: block;
  position: relative;
  margin: auto;
  width: 75vw;
  margin-bottom: 8rem;
}
.main section img {
  display: inline-block;
  margin: 8rem 0 -6rem 0;
  width: 100%;
  transition: .5s;
}
.main section p span{
  font-family: 'Cormorant Garamond', serif;
  font-weight: 700 !important;
}
.main section p{
  position: absolute;
  margin-top: 6rem;
  font-family: 'Cormorant Garamond', serif;
  font-weight: 400;
  font-style: italic;
  font-size: 0.9rem;
  transition: .5s;
}
.main section p:hover{
  font-weight: 700;
  font-style: normal;
}
.main section p a{
  color: #272727 !important;
  text-decoration: none;
}

}

@media screen and (min-width: 1024px) {

#side{
  position: fixed;
}
.main_t{
  position: fixed;
  top: 3rem;
  right: 6rem;
  margin: 0;
  font-family: 'Cormorant Garamond', serif;
  font-weight: 700;
  font-size: 10vw;
  color: #dadada;
}
.main{
  position: absolute;
  top: 12rem;
  right: 3rem;
  width: 75vw;
  column-count: 1;
  column-gap: 2rem;
}
.main section img {
  display: inline-block;
  margin: 0 0 2rem 15%;
  width: 60%;
}

.main section p span{
  font-family: 'Cormorant Garamond', serif;
  font-weight: 700 !important;
}
.main section p{
  font-family: 'Cormorant Garamond', serif;
  font-weight: 400;
  font-style: italic;
  margin: -1.5rem 0 2rem 15%;
  transition: .5s;
}
.main section p:hover{
  font-weight: 700;
  font-style: normal;
}
.main section p a{
  color: #272727 !important;
  text-decoration: none;
}

}
</style>