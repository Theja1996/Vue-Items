<template>
    <div class="items">
      <div class="item-inner">
          <div class="item-text-wrap">
              <h2 class="bg-text">{{Item.bgtext}}</h2>
          </div>
<div class="item-image-wrap">
    <img :src="Item.src" alt="tr dev" class="image"/>
</div>
<div class="item-detail">
    <h2>{{Item.title}}</h2>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci vero cumque, velit deleniti voluptatum animi praesentium rerum, id natus expedita earum, quisquam veritatis suscipit hic officia at soluta porro dolores!</p>
</div>
          
      </div>

    </div>
</template>

<script>
export default {
    name:'Item',
    props:['Item']
}
</script>

<style >
.items {
    flex: 1 1 33.333%;
    width: 100%;
    padding: 25px;
  }
  .item-inner {
    position: relative;
    padding: 25px;
    box-shadow: 0px 0px 16px rgba(0, 0, 0, 0.25);
   
  }
 .item-image-wrap .image {
    width: 100%;
    filter: drop-shadow(0px 0px 12px rgba(0, 0, 0, 0.25));
  }
 
</style>
