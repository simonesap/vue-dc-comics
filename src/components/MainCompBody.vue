<template>

  <div id="app">
     
     <main id="content">

       <h3>dc comics</h3>
       <h3>dc</h3>
       <h3>sites</h3>
       <h3>shop</h3>

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
              {
                characters: 'Characters',
                comics: 'Comics',
                movies: 'Movies',
                tv: 'TV',
                games: 'Games',
                videos: 'Videos',
                news: 'News'
              },
          ],

          dc: [
              {
                termsOfUSe: 'Terms Of USe',
                privacy: 'Privacy policy(New',
                adChoices: 'Ad Choices',
                advertising: 'Advertising',
                jobs: 'Jobs',
                subscriptions: 'Subscriptions',
                talent: 'Talent Workshops',
                cpsc: 'CPSC Certificates',
                ratings: 'Ratings',
                shopHelp: 'Shop Help',
                contactUs: 'Contact US'
              },
          ],

          sites: [
              {
                dc: 'DC',
                madMagazine: 'MAD Magazine',
                dcKids: 'DC Kids',
                dcUniverse: 'DC Universe',
                dcPowerVisa: 'DC Power Visa'
              },
          ],

          shop: [
              {
                shopDc: 'Shop DC',
                shopDcCollectibles: 'Shop DC Collectibles'
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
    };

    #content {
      background: url('../assets/img/footer-bg.jpg');
      height: 40vh;
    }

    h3 {
      text-transform: $text-uppercase;
      margin: 0 auto;
      color: $white;
    }
   
</style>