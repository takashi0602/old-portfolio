<template>
  <div>
    <div class="c-container row">
      <h1 class="h-title col">たかしのサイト</h1>
      <div class="h-links col-auto">
        <a href="/" class="h-link">トップ</a>
        <a href="/product" class="h-link">作品</a>
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
.c-container {
  padding-top: 15px;
  padding-bottom: 15px;
  display: flex;
}

.h {
  &-title {
    font-size: 1.5rem;
    margin: 0;
    line-height: 50px;
    @include desktop() {
      font-size: 2rem;
    }
  }
  &-link {
    font-size: 1rem;
    text-decoration: none;
    color: $black;
    padding: 0 5px;
    @include desktop() {
      font-size: 1.3rem;
    }
    &s {
      line-height: 50px;
    }
    &:hover {
      opacity: 0.5;
    }
  }
}
</style>
