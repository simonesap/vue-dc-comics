<template>
  <div id="app">

      <ul>
          <li v-for="(element, index) in menuNav" :key="index">
              {{element.button}}
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
  font-family: Avenir, Helvetica, Arial, sans-serif;
  @include reset-css
}

ul {
    @include reset-list;
    @include flexRow;
}

li {
    margin-inline: $mx-5;
    font-size: $font-size-small;
}

</style>