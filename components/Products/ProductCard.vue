<template>

  <div class="product">
    <div class="product__rating">
      <img src="images/reiting.png" />
      <span class="label">4.5</span>
    </div>
    <div class="product__cart">
      <img src="images/cart.png" />
    </div>
    <div class="product__img">
      <img src="images/products/louis-vuitton-nedium.png" />
    </div>
    <div class="product__details">
      <div class="product__details__title">
        {{newProduct.description}}
      </div>
      <div class="product__details__price">{{newProduct.price}} ₽</div>
    </div>
  </div>

</template>

<script>
export default {
name: "ProductCard",
  props: {
  product: {
    type: Object,
    default: {}
  }
  },
  computed: {
  newProduct() {
    return this.product
  }
  }
}
</script>

<style lang="scss">
.product {
  position: relative;
  border: 1px solid red;
  &__rating {
    position: absolute;
    top: 9px;
    left: 18px;
    .label {
      font-size: 10px;
      line-height: 13px;
      color: #f2c94c;
    }
  }
  &__cart {
    position: absolute;
    right: 18px;
    top: 9px;
    img {
      width: 12px;
      height: 13px;
    }
  }
  &__img {
    position: absolute;
    left: 0;
    right: 0;
    transform: translate(25%, 5%);
  }
  &__details {
    position: absolute;
    bottom: 16px;
    left: 16px;
    font-size: 14px;
    line-height: 18px;
    &__title {
      padding-bottom: 6px;
    }
    &__price {
      font-weight: 700;
    }
  }
}
</style>