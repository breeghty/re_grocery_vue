<template>
  <!-- header -->
  <header>
    <div class="innerHeader">
      <div class="menu">
        <button>Menu</button>
      </div>
      <h1 class="logo">
        re_
      </h1>
      <div class="rightSide">
        <button class="search">
          <img src="./assets/search_icon.png" alt="검색어를 입력하세요.">
        </button>
        <div class="cart">
          <p>cart (0)</p>
        </div>
      </div>
    </div>
  </header>
  <!-- 페이지 제목 -->
  <main>
    <p class="mainTit">re_<span class="pageTiT">{{pageTitle}}</span></p>
  </main>
  <!-- 상품섹션 -->
  <section class="products">
    <div class="leftMenu">
      <div class="topMenu">
        <p>All</p>
      </div>
    </div>
  </section>

</template>

<script>
import menuData from './data';

export default {
  name: 'App',
  data(){
    return{
      pageTitle: 'Pasta',
      menuData : menuData,
      topMenu : [
      'All', 'New Arrivals', 'Bestsellers', 'Staples'
      ],
      midMenu : [
      'Snacks', 'Herbs & Spices', 'Nuts & Seeds', 'Superfoods', 'Legumes',
    'Candy & Chocolate', 'Oils, Vinegars & Honey', 'Grains', 'Coffee & Tea', 
    'Cereal', 'Dried Fruit', 'Dehydrated', 'Pasta', 'Produce', 'Flours & Baking'
      ],
      botMenu : [
      'Bath & Body', 'Household', 'Reusables', 'In Store Only'
      ]
    }
  },
  components: {
    
  }
}
</script>

<style>
@import './css/reset.css';
@import './css/style.css';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #f7f6f2;
  width:100%;  
}
</style>
