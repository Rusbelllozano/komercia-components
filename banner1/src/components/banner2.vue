<template>
<div class="container">
  <div class="item item_image">
    <img :src="setting[0].photo">
  </div>
  <div class="item item_content">
    <div class="item texto">
      <h1>{{  setting[0].title }}</h1>
      <p>{{ setting[0].description }}</p>
      <a :href="setting[0].redirect_url">
        <button class="button">{{setting[0].button_text}}</button>
      </a>
    </div>
  </div>
  <div class="item item_content item_last">
    <div class="item texto">
      <h1>{{ setting[1].title }}</h1>
      <p>{{ setting[1].description }}</p>
      <a :href="setting[1].redirect_url">
        <button class="button">{{setting[1].button_text}}</button>
      </a>
    </div>
  </div>
  <div class="item item_image">
    <img :src="setting[1].photo">
  </div>
</div>
</template>

<script>

export default {
  name: 'banner2',
  props: ['setting'],
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style scoped>
.container{
  display: grid;
  grid-template: repeat(2, 1fr)/repeat(2, 1fr);
  max-width: 1366px;
  margin: 0 auto;
  font-family: helvetica;
}
.item{
  font-size: 12px;
}
.item .texto{
  max-width: 250px;
  width: 100%;
  text-align: justify;
  line-height: 22px;
}
.item .button{
  font-weight: bold;
  background-color: black;
  border: none;
  color: white;
  height: 30px;
  width: 150px;
  text-align: center;
  font-size: 12px;
  cursor: pointer;
  margin-top: 10px;
}
.item .button:hover{
  transform: scale(1.1);
}
.item_image{
  overflow: hidden;
}
.item_image img{
  height: 100%;
  object-fit: cover;
  width: 100%;
  z-index: 1;
}
h1{
  margin-top: 0px;
  margin-bottom: 10px;
}
.item_content{
  display: grid;
  align-items: center;
  justify-items: center;
  overflow: hidden;
  color: black;
  background-color: white;
}
@media screen and (max-width:800px) {
  .container{
    grid-template: repeat(4, 1fr)/ 1fr;
    max-height: 50%;
  }
  .item_last{
    order: 3;
  }
  .item .texto{
    width: initial;
    padding: 25px;
  }
}
</style>
