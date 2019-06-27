<template>
  <div>
    <div v-for="(item, index) in lists" :key="index">
      <div class="c-product">
        <div class="c-product__name">{{ item.name }}</div>
        <div class="c-product__detail">{{ item.detail }}</div>
        <a :href="item.url" class="c-product__link" target="_blank">
          <img :src="item.img" class="c-product__img c-image">
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    lists: {
      type: Array,
      default: []
    }
  }
}
</script>

<style lang="scss" scoped>
@import "~/assets/scss/foundation/mixin.scss";
@import "~/assets/scss/foundation/variable.scss";
.c-product {
  font-size: 0.8rem;
  padding: 0 15px;
  margin: 0 0 15px 0;
  border-bottom: 3px dashed $green;
  @include desktop() {
    font-size: 1.2rem;
  }
  &__name {
    margin-bottom: 10px;
    &:before {
      content: "";
      display: inline-block;
      width: 7px;
      height: 7px;
      background: $green;
      margin-right: 5px;
    }
  }
  &__detail {
    padding-left: 12px;
    margin-bottom: 15px;
  }
  &__link {
    cursor: pointer;
  }
  &__img {
    width: 100%;
    background-position: center center;
    border: 5px solid $green;
    border-radius: 20px;
    margin: 0 auto 20px auto;
  }
}
</style>
