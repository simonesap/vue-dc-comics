<template>
  <div id="app">

   <h5> Content goes here </h5>
  
  </div>
</template>

<script>


export default {
  name: 'JumboTron',

}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixin.scss';

    #app{
        background: black;
        height: 15vh;
        @include reset-css;
    }

    h5 {
      color: $white;
      @include container;
      padding: $p-30;
      font-size: $font-size-small;
    }

</style>