<template>

  <div id="app">
     
     <main id="content">
       
      <div id="container">

        <div id="col-1">
          <div>

            <div id="dcComics-shop-container">
              <h3>dc comics</h3>
              <ul>
                <li v-for="(element,index) in dcComics" :key="index">
                  <a href="#">{{element}}</a>
                </li>
              </ul>
            </div>
            <div>
              <h3 id="shop">shop</h3>
              <ul>
                <li v-for="(element,index) in shop" :key="index">
                  <a href="#">{{element}}</a>
                </li>
              </ul>
            </div>

          </div>
          
          <div>
            <h3>dc</h3>
            <ul>
              <li v-for="(element,index) in dc" :key="index">
                <a href="#">{{element}}</a>
              </li>
            </ul>
          </div>

          <div>
            <h3>sites</h3>
            <ul>
              <li v-for="(element,index) in sites" :key="index">
                <a href="#">{{element}}</a>
              </li>
            </ul>
          </div>

        </div>

        <div id="col-2">
          <div id="image"></div>
        </div>

      </div>
       
     </main>

  </div>

</template>

<script>

export default {
  name: 'MainCompBody',
  components: {
   
  },

  data() {
      return {

          dcComics: [
                'Characters',
                'Comics',
                'Movies',
                'TV',
                'Games',
                'Videos',
                'News'
          ],

          dc: [
                'Terms Of USe',
                'Privacy policy(New)',
                'Ad Choices',
                'Advertising',
                'Jobs',
                'Subscriptions',
                'Talent Workshops',
                'CPSC Certificates',
                'Ratings',
                'Shop Help',
                'Contact US'
          ],

          sites: [
                  'DC',
                  'MAD Magazine',
                  'DC Kids',
                  'DC Universe',
                  'DC Power Visa'
          ],

          shop: [
                  'Shop DC',
                  'Shop DC Collectibles'
          ],
      }
    }
}

</script>

<style lang="scss" scoped>
@import '../assets/style/mixin.scss';


    #app {
        @include reset-css;
        color: $white;
    };

    #content {
      background: url('../assets/img/footer-bg.jpg');
      background-size: cover;
      height: 50vh;
    }

    h3 {
      text-transform: $text-uppercase;
      padding-bottom: 15px;
      margin: 0 auto;
    }

    #container {
      @include container;
      @include flexBetween;
    }

    #col-1 {
      padding: $p-30;
      width: 50%;
      @include flexRow;
      div {
        align-items: center;
        ul {
          padding: 10px;
          @include reset-list;
          @include flexColumn;
          li {
            width: 150px;
            a {
              @include textDecorationNone;
              color: $white;
              font-size: $font-size-ultraSmall;
            }
          }
        };
      };
    }

    #col-2 {
      width: 50%;
      height: 50vh;
       #image {
        margin: 0 auto;
        padding: 0;
        background: url('../assets/img/dc-logo-bg.png');
        background-size: cover;
        background-position: center;
        height: 100%;
        width: 550px;
       }
      
    }

    #shop {
      padding-top: 15px;
    }
   

   
</style>