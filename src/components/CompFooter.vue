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
  name: 'CompFooter',
  data() {
      return {
          icon: [
                require('@/assets/img/footer-facebook.png'),
                require('@/assets/img/footer-twitter.png'),
                require('@/assets/img/footer-youtube.png'),
                require('@/assets/img/footer-pinterest.png'),
                require('@/assets/img/footer-periscope.png'),
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

    #container {
        @include flexBetween;
        @include container;
        padding: 20px;
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
        li {
            margin: $mx-8;
        }
    }

    button {
        background: transparent;
        border: 2px solid $azurre;
        padding: 10px;
        color: $white;
        font-size: $font-size-ultraSmall;
        text-transform: $text-uppercase;
    }

    h3 {
        text-transform: $text-uppercase;
        color: $azurre;
        font-size: $font-size-small;
        margin-right: 30px;
    };

    img {
        width: 35px;
        height: 35px;
    }

</style>