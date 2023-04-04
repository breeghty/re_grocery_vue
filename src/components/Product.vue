<template>
  <div class="box">
    <div class="imgBox">
      <img :src="productName.image" alt="상품의 이미지입니다.">
      <button class="addBtn">Add to cart</button>
      <div class="addCart">
        <!-- components -->
      </div>
    </div>
    <div class="txtBox">
      <p class="proTit">{{productName.title}}</p>
      <p class="price">$1.98-3.95</p>
      <div class="optBox">
        <p v-for="(opt, i) in options" :key="opt">{{options[i]}}</p>
      </div>
    </div>
  </div>
</template>

<script>


export default {
  name: 'productList',
  data(){
    return{
      options : [ 'Organic', 'Non-GMO', 'Vegan'],
      
    }
  },
  props : {
    productName : Object,
  }

}
</script>

<style>

</style>