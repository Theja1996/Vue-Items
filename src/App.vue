<template>
  <main id="app" >
  <section class="items">
<Item
v-for="Item in products" 
:key="Item.color"
:Item="Item" />
  </section>
  </main>
</template>

<script>
import Item from './components/Item.vue'

export default {
  name: 'App',
  components:{
   Item
   
  },
  data(){
    return{
      products:[
        {
          title: 'Nike Air Max',
          color: 'green',
          bgtext: 'NIKE',
          src: require('./assets/green-shoe.png')
        },
        {
          title: 'Nike flex',
          color: 'blue',
          bgtext: 'AIR',
          src: require('./assets/blue-shoe.png')
        },
        {
          title: 'Nike Roche Runs',
          color: 'pink',
          bgtext: 'MAX',
          src: require('./assets/pink-shoe.png')
        }
      ]

      
    }
  }
  
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body {
    font-family: 'montseratt', sans-serif;
  }

 main {
    width: 100vw;
    min-height: 100vh;
    overflow: hidden;
    background-color: #EEE;
    display: flex;
    justify-content: center;
    align-items: center;
  }

 .items {
    display: flex;
    max-width: 1280px;
    padding: 25px;
    margin: 0 auto;
  }
</style>
