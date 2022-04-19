<template>
  <div id="app">
      
      <div id="main">
          <ul>
              <li v-for="(element,index) in select" :key="index">
                  <img :src="element.url" role="button">
                  <a href="#">{{element.name}}</a>
                  <!-- <img src="../assets/img/buy-comics-digital-comics.png" alt=""> -->
              </li>
          </ul>
      </div>

  </div>
</template>

<script>

export default {
  name: 'MainMenuComp',
  components: {
   
  },

  data() {
      return {
          select: [
              {
                name: 'DIGITAL COMICS',
                url: require('@/assets/img/buy-comics-digital-comics.png'),
              },
              {
                name: 'DC MERCHANDISE',
                url: require('@/assets/img/buy-comics-merchandise.png'),
              },
              {
                name: 'SUBSCRIPTION',
                url: require('@/assets/img/buy-comics-subscriptions.png'),
              },
              {
                name: 'COMIC SHOP LOCATOR',
                url: require('@/assets/img/buy-comics-shop-locator.png'),
              },
              {
                name: 'DC POWER VISA',
                url: require('@/assets/img/buy-dc-power-visa.svg'),
              },
          ],
      }
    }
}

</script>

<style lang="scss" scoped>
@import '../assets/style/mixin.scss';

    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        @include reset-css
    }

    #main {
        background: $azurre;
    };

    ul {
        @include reset-list; 
        @include container;
        @include flexBetweenAlign;
    }
    
    li {
        width: 40%;
        padding: 20px;
        @include flexRow;
        align-items: center;
          a {
          @include textDecorationNone;
          color: $white;
          }
          img {
            width: 45px;
            height: 55px;
            margin: 5px;
          }
    }

</style>