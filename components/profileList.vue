<template>
  <div>
    <div v-for="(item, index) in lists" :key="index">
      <div class="c-profile row align-items-center">
        <span class="col-4">{{ item.name }}</span>
        <span class="col-8">{{ item.detail }}</span>
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
.c-profile {
  font-size: 0.8rem;
  margin: 0 0 15px 0;
  border-bottom: 3px dashed $green;
  @include desktop() {
    font-size: 1.2rem;
  }
}
</style>
