<template>
  <div id="app">
      
      <div id="main">
          <ul>
              <li v-for="(element,index) in select" :key="index">
                  <img :src="element.icon" :alt="element.name">
                  <img src="../assets/img/buy-comics-digital-comics.png" alt="">
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
                name : 'DIGITAL COMICS',
                icon : '../src/assets/img/buy-comics-digital-comics.png',
              },
              {
                name: 'DC MERCHANDISE',
                icon: '../src/assets/img/buy-comics-merchandise.png',
              },
              {
                name: 'SUBSCRIPTION',
                icon: '../src/assets/img/buy-comics-subscriptions.png',
              },
              {
                name: 'COMIC SHOP LOCATOR',
                icon: '../src/assets/img/buy-comics-shop-locator.png',
              },
              {
                name: 'DC POWER VISA',
                icon: '../src/assets/img/buy-dc-power-visa.svg',
              },
          ],
          counter: 0,
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
        @include flexBetween;
    }
    
    li {
        padding: $p-30;
    }

</style>