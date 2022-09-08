<template>
  <ul class="categories">
    <li
        class="categories__item"
        v-for="category in newCategories"
        :key="category.id">
      {{category.title}}
    </li>
  </ul>
</template>

<script>
export default {
  name: "SideMenu",
  props: {
    categories: {
      type: Array,
      default: [],
    },
  },
  computed: {
    newCategories() {
      return this.categories;
    }
  }
};
</script>

<style lang="scss">
.categories {
  width: 161px;
  &__item {
    padding: 8px 0px;
    font-size: 16px;
  }
}
</style>
