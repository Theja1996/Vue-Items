<template>
    <div class="item">
      <div :class="'item-inner  ' + item.color">
          <div class="item-text-wrap">
              <h2 class="bg-text">{{item.bgtext}}</h2>
          </div>
<div class="item-image-wrap">
    <img :src="item.src" alt="tr dev" class="image"/>
</div>
<div class="item-detail">
    <h2>{{item.title}}</h2>
<p>{{item.intro}}</p>

</div>
          
      </div>

    </div>
</template>

<script>
export default {
    name:'Item',
    props:['item']
}
</script>

<style >
.item {
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

  .item-inner.green {
    background-image: linear-gradient(to bottom right, #24D484, #116432);
  }
 .item-inner.blue {
    background-image: linear-gradient(to bottom left, #24D484, #2474C4 70%);
  }
  .item-inner.pink {
    background-image: linear-gradient(to bottom right, #F444A4, #1168D4);
  }
  .item-text-wrap {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 0;
    overflow: hidden;
    perspective: 1000px;
  }
   .item-text-wrap h2 {
    color: #313131;
    font-size: 128px;
    font-weight: 900;
    opacity: 0.2;
    transform-origin: center;
  }
   .item-image-wrap {
    position: relative;
    z-index: 1;
    transform-origin: center;
  }
  .item-detail {
    background-color: #FFF;
    padding: 25px;
    margin: 0px -25px -25px;
  }
  .item-detail h2 {
    font-size: 24px;
    font-weight: 700;
    color: #676767;
    margin-bottom: 15px;
  }
  .item-detail p {
    font-size: 14px;
    line-height: 1.5;
    font-weight: 300;
    color: #676767;
  }
  .green{
   background-color: #41B883;
}
.blue{
   background-color: #35495E;
}
</style>
