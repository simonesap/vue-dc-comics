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

<style lang="scss">
@import '../assets/style/mixin.scss';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

ul {
    @include flexRow;
}

li {
    margin-inline: $mx-5;
}

</style>