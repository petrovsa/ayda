<template>
  <div class="main">
    <div class="header">
      <div class="header__title">Title</div>
      <dir class="header__cart">
        <img src="images/cart.png" />
      </dir>
    </div>
    <div class="catalog">
      <div class="catalog__header">
        <div class="catalog__title">Каталог</div>
        <div class="catalog__sorting">Сортировать по цене</div>
      </div>
      <div class="catalog__sidebar">
        <ul class="categories">
          <li class="categories__item">Рюкзаки</li>
          <li class="categories__item">Футболки</li>
          <li class="categories__item">Рубашки</li>
        </ul>
        <div class="catalog__products">
          <div class="catalog__products__block"></div>
          <div class="catalog__products__block"></div>
          <div class="catalog__products__block"></div>
          <div class="catalog__products__block"></div>
          <div class="catalog__products__block"></div>
          <div class="catalog__products__block"></div>
          <div class="catalog__products__block"></div>
          <div class="catalog__products__block"></div>
          <div class="catalog__products__block"></div>
          <div class="catalog__products__block"></div>
          <div class="catalog__products__block"></div>
          <div class="catalog__products__block"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      post: {
        title: "Hello Magazine",
        description: "It`s Nuxt project",
      },
    };
  },
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
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid black;
    &__title {
      font-weight: 700;
      font-size: 22px;
      line-height: 28px;
    }
  }
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
      .categories {
        width: 161px;
        &__item {
          padding: 8px 0px;
          font-size: 16px;
        }
      }
    }
    &__products {
      width: 100%;
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      grid-auto-rows: 272px;
      gap: 16px;
      &__block {
        border: 1px solid red;
      }
    }
  }
}
</style>
