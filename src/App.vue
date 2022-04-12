<template>
  <div id="app">

    <header>

      <LogoComp/>

      <NavComp/>
    
    </header>
    
  </div>
</template>

<script>
import LogoComp from './components/LogoComp.vue';
import NavComp from './components/NavComp.vue';

export default {
  name: 'App',
  components: {
    LogoComp,
    NavComp,
  }
}
</script>

<style lang="scss">
@import './assets/style/mixin.scss';

   header {
        @include container;
        @include flexBetween;
        margin-top: $mt-50;
   }

</style>
