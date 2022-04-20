<template>

  <ul id="app">
    <li class="container p-y-30">
      <img :src="img" alt="">
      <h3>{{title}}</h3>
      <div id="price">{{price}}</div>
      <div id="type">{{type}}</div>
    </li>
  </ul>

</template>

<script>


export default {
  name: 'ProductComp',
    props: {
      img: String,
      price: String,
      title: String,
      type: String,
    }
}

</script>

<style lang="scss" scoped>
@import '../assets/style/mixin.scss';

    #app{
        @include reset-css;
        background: $footer-brown;
        @include flexRowAlign;
        color: $white;

  ul {
    @include reset-list;
    li {
      margin-left: 10px;
      margin-right: 10px;
      height: 400px;
      
    }
  }

  li:hover {
    box-shadow: 0px 5px 10px 20px inset $azurre;
    border-radius: 5%;
    cursor: pointer;
  }

      img {
        width: 170px;
        height: 220px;
        padding: 5px;
      }
    }

    h3 {
      width: 100px;
    }

    #price {
      margin-bottom: 10px;
    }

    #type {
      text-transform: uppercase;
      color: red;
    }

</style>