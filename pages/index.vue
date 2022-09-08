<template>
  <div class="main">
    <AydaHeader />
    <div class="catalog">
      <div class="catalog__header">
        <div class="catalog__title">Каталог</div>
        <div class="catalog__sorting">Сортировать по цене</div>
      </div>
      <div class="catalog__sidebar">
        <SideMenu :categories="categories" />
        <div class="catalog__products">
          <ProductCard v-for="product in products" :key="product.id" :product="product"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AydaHeader from "../components/AydaHeader";
import SideMenu from "../components/SideMenu";
import ProductCard from "../components/Products/ProductCard";
export default {
  name: "IndexPage",
  asyncData(){
    return {
      categories: [
        { id: 1, title: "Рюкзаки", product: [
            {id: 11, 'description': 'Рюкзак Louis Vuitton Discovery', 'price': 150000},
            {id: 12, 'description': 'Рюкзак Louis Vuitton Discovery', 'price': 150000},
            {id: 13, 'description': 'Рюкзак Louis Vuitton Discovery', 'price': 150000},
            {id: 14, 'description': 'Рюкзак Louis Vuitton Discovery', 'price': 150000},
            {id: 15, 'description': 'Рюкзак Louis Vuitton Discovery', 'price': 150000},
            {id: 16, 'description': 'Рюкзак Louis Vuitton Discovery', 'price': 150000},

          ] },
        { id: 2, title: "Футболки" },
        { id: 3, title: "Рубашки" },
      ],
    }
  },
  components: {
    ProductCard,
    AydaHeader,
    SideMenu,
  },
  computed: {
    products(){
      return this.categories[0].product;
    }
  }
};
</script>
<style lang="scss">
ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

.main {
  font-family: "Poppins", sans-serif;
  margin: 0 auto;
  width: 1265px;
  padding: 0px 88px;

  .catalog {
    &__header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-top: 32px;
    }
    &__title {
      font-size: 32px;
      line-height: 41px;
      font-weight: 700;
    }
    &__sorting {
      font-size: 16px;
      line-height: 21px;
    }
    &__sidebar {
      display: flex;
    }
    &__products {
      width: 100%;
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      grid-auto-rows: 272px;
      gap: 16px;

    }
  }
}
</style>
