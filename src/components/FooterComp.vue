<template>
  <div id="app">

    <div id="container">

        <div id="col-1">
            <button>sign-up now!</button>
        </div>

        <div id="col-2">
            <div>
                    <h3>follow us</h3>
            </div>
            
            <div>
                <ul id="list">
                    <li v-for="(element,index) in icon" :key="index">
                        <img :src="element" alt="Social">
                    </li>
                </ul>
            </div>
        </div>

    </div>
      
  
  </div>
</template>

<script>


export default {
  name: 'FooterComp',
  data() {
      return {
          icon: [
                '../assets/img/footer-facebook.png',
                '../assets/img/footer-twitter.png',
                '../assets/img/footer-youtube.png',
                '../assets/img/footer-pinterest.png',
                '../assets/img/footer-periscope.png',
          ]
  }

}
}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixin.scss';

    #app {
    @include reset-css;
    }

    img {
        width: 50px;
        height: 50px;
    }

    #container {
        @include flexBetween;
        @include container;
    }

    #col-1 {
        padding: 20px
    }

    #col-2 {
        @include flexRowAlign;
    }

    #list {
        @include reset-list;
        @include flexRow;
    }

    button {
        background: none;
        border: 2px solid $azurre;
        padding: 10px;
        color: $white;
        text-transform: $text-uppercase;
    }

    h3 {
        text-transform: $text-uppercase;
        color: $azurre;
    }

</style>