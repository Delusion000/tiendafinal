<template>
    <div class="caja1">
      <div class="cabecera">
        <h1>TWELVE ES TWELVE</h1>
        <div class="tiendabutton"><router-link class="button2" to="/shop">Tienda/Shop</router-link></div>
      </div>
    </div>
    <div class="caja2">
      <h1><router-link to="/shop">Tienda/Shop</router-link></h1>
    </div>
    <div class="publicidad">
      <div class="imagenPublicidad"><img src="../assets/jinnkpublicidad.jpg" /></div>
      <div class="infoPublicidad">
        <p @click="$router.push('Tienda')">Especial edition tshirt</p>
        <p>40 &euro;</p>
      </div>
    </div>
    <div class="publicidad">
      <div class="imagenPublicidad"><img src="../assets/ovalopublicidad.jpg" /></div>
      <div class="infoPublicidad">
        <p @click="$router.push('Tienda')">Camiseta oversize</p>
        <p>20 &euro;</p>
      </div>
    </div>
    <div class="caja3">
      <div class="textoCaja3">
        <p>inexpertos creando</p>
        <p>Maravillas</p>
        <p>para que vistas, con estilo</p>
      </div>
      
    </div>
  
</template>

<script>
import {mapState} from 'vuex'

export default {
  name: 'Home',
  computed: {
    ...mapState(['articulos'])
  }
  
}
</script>

<style scoped>
  .caja1 {
    height: 78vh;
    width: 100%;
    background-image: url("../assets/4.jpg");
    background-size: cover;
    display: table;
    background-attachment: fixed;

    /* Flex */
    display: flex;
    justify-content:center;
    align-items: center;
    flex-direction:row;
    flex-wrap:wrap;
  }
  .caja2 {
    height: 90vh;
    width: 50%;
    background-image: url("../assets/home1.jpg");
    background-size: contain;
    display: table;
    background-attachment: fixed;
  }

  .caja2 h1 {
    text-align: center;
    display: table-cell;
    vertical-align: middle;
  }
  .caja3 {
    height: 90vh;
    width: 50%;
    background-image: url("../assets/home2.jpg");
    background-size: contain;
    display: table;
    background-attachment: fixed;
  }
  .caja3 .textoCaja3 {
    text-align: center;
    display: table-cell;
    vertical-align: middle;
  }

  .cabecera h1 {
    font-family: arial bold;
    font-size: 40px;
    color: white;
    width:100%;
  }

  .destacados {
    height: 90vh;
    width:100%;
  }
  .publicidad{
    height: 90vh;
    width:50%;
    background-color: #1c54;
    align-items: center;
    display: flex;
    justify-content: center;
    flex-direction:column;
  }
  .imagenPublicidad img {
    width: 50%;
  }

  a.button2{
    display:inline-block;
    padding:0.5em 4em;
    border:0.16em solid #FFFFFF;
    margin: 0 0.3em 0.3em 0;
    box-sizing: border-box;
    text-decoration:none;
    color: white;
    text-align: center;
    font-size:20px;
    transition: all 0.15s;
  }

 a.button2:hover{
   color: orange;
   border-color: orange;
   background: white;
 }

 @media all and (max-width:30em){
   a.button2{
     display:block;
     margin:0.4em auto;
   }
 }
 a {
   color: white;
 }
 .caja3 p:nth-child(2){
   color: white;
   font-style: oblique;
   font-size: 35px;
 }
 .caja3 p:nth-child(1){
   color: white;
   font-weight: bolder;
   font-size: 25px;
 }
  .caja3 p:nth-child(3){
   color: white;
   font-weight: bolder;
   font-size: 25px;
 }
 .textoCaja3 a {
   color: white;
 }
 .infoPublicidad  p:nth-child(2) {
   color: orange;
   margin-top:10px;
 }
 .infoPublicidad  {
   margin-top: 20px;
 }
</style>
