<template>
  <div id="app">

      <ul>
          <li v-for="(element, index) in menuNav" :key="index">
              <a href="#">{{element.button}}</a>
          </li>
      </ul>
      <!-- @mouseover="mouseOver" -->
  <!-- :class="(element == 'inactive') ? 'border-b' : '' " -->
  </div>
</template>

<script>


export default {
  name: 'NavCOmp',
  data() {
      return {
          menuNav: [
              {
                button: 'CHARACTERS',
                url: ''
                // status: 'inactive',
              },
              {
                button: 'COMICS',
                // status: 'inactive',
              },
              {
                button: 'MOVIES',
                // status: 'inactive',
              },
              {
                button: 'TV',
                // status: 'inactive',
              },
              {
                button: 'GAMES',
                // status: 'inactive',
              },
              {
                button: 'COLLECTIBLES',
                // status: 'inactive',
              },
              {
                button: 'VIDEOS',
                // status: 'inactive',
              },
              {
                button: 'FANS',
                // status: 'inactive',
              },
              {
                button: 'NEWS',
                // status: 'inactive',
              },
              {
                button: 'SHOP',
                // status: 'inactive',
              },
          ],
          // Stato di default dell'active per mostrare il bordo all'hover 
        //   active: true,
    }
  
  },
//   methods: {
//       // Funzione hover sull'elemento
//       mouseOver: function(){
//                 if(this.active = !this.active){
//                     this.active = true;
//                 }  else {
//                     this.active = false
//                 }
//             },

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
    height: 100%;
}

li {
    margin-inline: $mx-12;
    font-size: $font-size-smallSmall;
    padding-bottom: calc(30px - 4px);
    a {
        @include textDecorationNone;
        color: black;
        font-weight: bold;
        }
};

li:hover {
  border-bottom: 4px inset $azurre;
}

    // .border-b {
    //     border-bottom: 3px solid #0180ff;
    // }

</style>