<template>
  <div id="app">

    <header>

      <LogoComp/>

      <NavComp id="nav"/>
    
    </header>

    <div id="jumbo">

      <JumboTron/>

    </div>

    <main>

      <MainMenuComp/>
  
      <MainCompBody/>

    </main>

  </div>
</template>

<script>
import LogoComp from './components/LogoComp.vue';
import NavComp from './components/NavComp.vue';
import JumboTron from './components/JumboTron.vue';
import MainMenuComp from './components/MainMenuComp.vue';
import MainCompBody from './components/MainCompBody.vue';

export default {
  name: 'App',
  components: {
    LogoComp,
    NavComp,
    JumboTron,
    MainMenuComp,
    MainCompBody,
  }
}
</script>

<style lang="scss" scoped>
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
      @include flexBetween;
      margin: $my-50 auto;
  }

  
   

</style>
