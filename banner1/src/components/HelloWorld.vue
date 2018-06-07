<template>
  <div class="hello">
    <div class="item header">
<img src="../assets/head.jpg">
      <div class="item">
          MID SEASON
         <h1> SALE</h1>
         UP TO
        <p> 50% OFF</p>
     </div>
     <button class="button ">SHOP NOW</button>
   </div>

    <div class="item left">
        <img src="../assets/left.jpg">
        <div class="item">
          MID SEASON SALE<br>
          SALE UP TO 50% OFF
        </div>
        <button class="button">SHOP NOW</button>
    </div>

    <div class="item contenido">
      <img src="../assets/center.jpg">
      <div class="item">
        NEW ARRIVALS<br>
        BROWSE OUR NEW COLLECTIONS
      </div>
      <button class="button">BROWSE</button>
    </div>
    <div class="item right">
      <img src="../assets/right.jpg">
      <div class="item">
        GET THE LOOK<br>
        NOT READY FOR SUMMER?
      </div>
      <button class="button">GET THE LOOK</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello{

      display: grid;
      grid-template:repeat(2,1fr) / repeat(3,1fr);
      height: 120em;
      grid-template-areas:"header  header header"
                          "left contenido right" ;
      font-family: helvetica ;
      font-weight: bold;
      max-width: 1024px;
      max-height: 720px;



}
.item{
      display: grid;

      }
.item .item{
      height: 2ms;
      width: 100%;
      background: transparent;
      padding: 10px 20px 10px 0px;
      text-align: left;
      font-size: 12px;


}
.header .item{
      border: solid white;
      height:150px;
      width: 150px;
      border-width: 10px;
      border-style: double;
      padding: 10px 20px;
      text-align: center;
      font-size: 16px;
      z-index: 2;
}
.header{
      overflow: hidden;
      position: relative;
      grid-area: header;
      padding-top: 50px;
      padding-left:100px;
      color: white;
      background-color: black;
      background-size: cover;

  }
  .header img{
    max-height: 720px;

        object-fit: contain;
        position: absolute;
        top: 0;
        width: 100%;
        opacity: .5;
        z-index: 1;
  }
.contenido{
      overflow: hidden;
      position: relative;
      grid-area: contenido;
      height: 125px;
      padding-top: 10px;
      padding-left:50px;



  }
.contenido img{

      position: absolute;
      top: 0;
      width: 100%;
      object-fit: cover;
      opacity: .5;
      z-index: -1;
}
.left{
      overflow: hidden;
      position: relative;
      grid-area: left;
      height: 125px;
      padding-top: 10px;
      padding-left:50px;
      float: left;
    }
.left img{

      position: absolute;
      top: 0;
      width: 100%;
      object-fit: cover;
      opacity: .5;
      z-index: -1;
}
.right{
      overflow: hidden;
      position: relative;
      grid-area: right;
      height: 125px;
      padding-top: 10px;
      padding-left:50px;
      float: left;
    }
.right img{

      position: absolute;
      top: 0;
      width: 100%;
      object-fit: cover;
      opacity: .5;
      z-index: -1;
}
.button {
      font-weight: bold;
      background-color: black;
      border: none;
      color: white;
      height: 30px;
      width: 100px;
      text-align: center;
      font-size: 12px;
      cursor: pointer;

}
.header .button{
      height: 40px;
      width: 150px;
      background-color: brown;
      font-size: 15px;
      margin: calc(110px - 75px);
      z-index: 2;

}
</style>
