<template>
  <div class="header">
    <div class="header__title">Title</div>
    <div class="header__cart">
      <img src="images/cart.png" />
    </div>
  </div>
</template>

<script>
export default {
name: "AydaHeader"
}
</script>

<style lang="scss">
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
</style>