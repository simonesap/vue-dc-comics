<template>
  <div id="app">

      <ul>
          <li v-for="(element, index) in menuNav" :key="index">
              <a href="#">{{element.button}}</a>
          </li>
      </ul>
  
  </div>
</template>

<script>


export default {
  name: 'NavCOmp',
  data() {
      return {
          menuNav: [
              {
                button: 'CHARACTERS'
              },
              {
                  button: 'COMICS'
              },
              {
                  button: 'MOVIES'
              },
              {
                  button: 'TV'
              },
              {
                  button: 'GAMES'
              },
              {
                  button: 'COLLECTIBLES'
              },
              {
                  button: 'VIDEOS'
              },
              {
                   button: 'FANS'
              },
              {
                  button: 'NEWS',
              },
              {
                  button: 'SHOP',
              },
          ],
  }

}
}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixin.scss';

#app {
  @include reset-css
}

ul {
    @include reset-list;
    @include flexRow;
}

li {
    margin-inline: $mx-12;
    font-size: $font-size-smallSmall;
    a {
        @include textDecorationNone;
        color: black;
        font-weight: bold;
        }
}

</style>