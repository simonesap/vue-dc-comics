<template>
  <div id="app">

    <header class="my-20">

      <LogoComp/>

      <NavComp id="nav"/>
    
    </header>

    <div id="jumbo">

      <JumboTron/>

    </div>

    <main>

      <MainMenuComp id="main-1" />
  
      <MainCompBody id="main-2" />

    </main>

    <footer>

      <CompFooter id="footer" />

    </footer>

  </div>

</template>
    
    
<script>
import LogoComp from './components/LogoComp.vue';
import NavComp from './components/NavComp.vue';
import JumboTron from './components/JumboTron.vue';
import MainMenuComp from './components/MainMenuComp.vue';
import MainCompBody from './components/MainCompBody.vue';
import CompFooter from './components/CompFooter.vue';


export default {
  name: 'App',
  components: {
    LogoComp,
    NavComp,
    JumboTron,
    MainMenuComp,
    MainCompBody,
    CompFooter,
  },
  
}
</script>

<style lang="scss" scoped>
@import './assets/style/general.scss';
@import './assets/style/mixin.scss';
@import url('https://fonts.googleapis.com/css2?family=Fira+Sans+Extra+Condensed&display=swap');

  @font-face {
  font-family: DcFandom;
  src: url(assets/fonts/DcFandom-orr4.ttf);
  }

  #app {
    @include reset-css;
  }

  #nav {
    font-family: 'Fira Sans Extra Condensed', sans-serif;
  }

  #jumbo{
    font-family: DcFandom;
  }

  header {
      @include container;
      @include flexBetweenAlign;
  }

  #main-1 {
    font-family: 'Fira Sans Extra Condensed', sans-serif;
    color: $white;
  }

  #main-2 {
    font-family: 'Fira Sans Extra Condensed', sans-serif;
    color: $white;
  }

  #footer {
    background: $footer-brown;
    font-family: 'Fira Sans Extra Condensed', sans-serif;
  }
  
   

</style>
