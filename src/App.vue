<template>
  <div id="app">
      <nav class="navbar navbar-expand navbar-dark fixed-top" id="mainNav">
    <div class="container">
      <a class="navbar-brand js-scroll-trigger" href="#page-top">Bjørg's's Website</a>
      <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
        Menu
        <i class="fas fa-bars"></i>
      </button>
      <div class="collapse navbar-collapse" id="navbarResponsive">
        <ul class="navbar-nav text-uppercase ml-auto">          
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#cv">Portfolio</a>
          </li>
          <li class="nav-item">&nbsp;&nbsp;&nbsp;&nbsp;</li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#json">Contact Info</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Header -->
  <header class="masthead">
    <div class="container">
      <div class="intro-text">
        <div class="intro-lead-in">Welcome To My Website!</div>
        <div class="intro-heading text-uppercase">It's Nice To Meet You</div>
      </div>
    </div>
  </header>

 

 <!-- BjorgPortfolio -->

  <bjorgPortfolio>  </bjorgPortfolio>
 

 

  <!-- Contact info -->

  <contactInfo>  </contactInfo>

  

 

  
  </div>
</template>

<script>

import HaraldCV from './components/HaraldCV.vue'
import MovieData from './components/MovieData.vue'

export default {
  name: 'app',
  components: {
    HaraldCV,
    MovieData
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.intro-lead-in,
.intro-heading.text-uppercase {
  text-shadow: 0px 0px 7px rgba(0, 0, 0, 0.521);
}

</style>
