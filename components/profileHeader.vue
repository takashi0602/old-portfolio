<template>
  <div>
    <div class="h-header">
      <div class="h-boxShadow">
        <div class="c-container row">
          <h1 class="h-title col">たかしのサイト</h1>
          <div class="h-pcMenu col-auto">
            <nuxt-link to="/" class="h-pcMenu__link">トップ</nuxt-link>
            <nuxt-link to="/product" class="h-pcMenu__link">作品</nuxt-link>
          </div>
          <div class="h-spMenu col-auto">
            <i class="material-icons" @click="clickMenu">{{ iconName }}</i>
          </div>
        </div>
      </div>
      <div v-if="toggleMenu" class="h-spMenu__links">
        <nuxt-link to="/" class="h-spMenu__dropLink" @click.native="clickLink">トップ</nuxt-link>
        <nuxt-link to="/product" class="h-spMenu__dropLink" @click.native="clickLink">作品</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      toggleMenu: false,
      iconName: "menu"
    }
  },
  methods: {
    clickMenu() {
      this.toggleMenu = !this.toggleMenu
      this.iconName = this.iconName === "menu" ? "close" : "menu"
    },
    clickLink() {
      console.log("hoge")
      this.toggleMenu = false
      this.iconName = this.iconName === "menu" ? "close" : "menu"
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
  &-boxShadow {
    box-shadow: 0 3px 1px -1px rgba(0,0,0,0.4);
  }
  &-header {
    position: fixed;
    width: 100%;
    background: $white;
  }
  &-title {
    font-size: 1.5rem;
    margin: 0;
    line-height: 30px;
    @include desktop() {
      font-size: 2rem;
    }
  }
  &-pcMenu {
    display: none;
    line-height: 30px;
    @include desktop() {
      display: block;
    }
    &__link {
      font-size: 1.3rem;
      text-decoration: none;
      color: $black;
      padding: 0 5px;
      &:hover {
        opacity: 0.5;
      }
    }
  }
  &-spMenu {
    display: block;
    line-height: 30px;
    @include desktop() {
      display: none;
    }
    &__links {
      display: block;
      @include desktop() {
        display: none;
      }
    }
    &__dropLink {
      display: block;
      font-size: 1rem;
      text-decoration: none;
      color: $black;
      padding: 20px 20px;
      width: 100%;
      border-bottom: 1px solid $gray;
      &:hover {
        opacity: 0.5;
      }
    }
  }
}
</style>
