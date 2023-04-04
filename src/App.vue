<template>
  <!-- header -->
  <header>
    <div class="innerHeader">
      <nav>
        <button>menu</button>
      </nav>
      <h1 class="logo">
        re__
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
    <!-- 사이드 메뉴 -->
    <div class="leftMenu">
      <div class="topMenu">
        <menuList v-for="(menu, i) in topMenu" :key="menu" :menuTit="topMenu[i]"></menuList>
      </div>
      <div class="midMenu">
        <menuList v-for="(menu, i) in midMenu" :key="menu" :menuTit="midMenu[i]"></menuList>
      </div>
      <div class="botMenu">
        <menuList v-for="(menu, i) in botMenu" :key="menu" :menuTit="botMenu[i]"></menuList>
      </div>
    </div>
    <!-- 상품정보 -->
    <div class="productInfo">
      <productList v-for="(pdt, i) in productsName" :key="pdt" :productName="productsName[i]"></productList>
    </div>
  </section>
  <!-- 카테고리 -->
  <section class="category">
    <h3>Categories</h3>
    <div class="categoryList">

    </div>
  </section>
  <!-- footer -->
  <footer>
    <div class="innerFooter">
      <div class="footerTopLeft">
        <h1 class="footer_logo">
          re__
        </h1>
      </div>
      <div class="footerTopRight">
        <p>
          re__makes it easier and more affordable to shop sustainably. To do better than recycling. To say no to plastic altogether. Thanks to you, we’ve diverted over 250,000 items of packaging from landfill since opening on Earth Day 2020.
        </p>
      </div>
      <div class="footerBotLeft">
        <h4>Let's Keep in Touch</h4>
        <p>Sign-up for 10% off your first online order</p>
        <input type="text" placeholder="Email">
        <ul class="mark">
          <li v-for="list in 3" :key="list"><img src="./assets/for_the_planet.png" alt="for the planet의 인증 마크 입니다."></li>
        </ul>
      </div>
      <div class="footerBotRight">
        <ul class="list_1">
          <li v-for="(link,i) in link_list_1" :key="link">{{ link_list_1[i] }}</li>
        </ul>
        <ul class="list_2">
          <li v-for="(link,i) in link_list_2" :key="link">{{ link_list_2[i] }}</li>
        </ul>
        <ul class="list_3">
          <li v-for="(link,i) in link_list_3" :key="link">{{ link_list_3[i] }}</li>
        </ul>
      </div>
      <p class="copyright">@ 2022 re grocery inc. All rights reserved.</p>
    </div>
  </footer>

</template>

<script>
// import menuData from './data';
import productsName from './products';
import menuList from './components/Menu.vue';
import productList from './components/Product.vue';

export default {
  name: 'App',
  data(){
    return{
      pageTitle: 'Pasta',
      // menuData : menuData,
      productsName : productsName,
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
      ],
      link_list_1:[
        'Our Ethos', 'FAQs', 'B Corp', 'Careers', 'E-Gift Cards'
      ],
      link_list_2:[
        'Locations', 'Instagram', 'TikTok', 'Contact'
      ],
      link_list_3 : [
        'Account', 'Privacy', 'Terms'
      ]
    }
  },
  components: {
    menuList : menuList,
    productList : productList,
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
