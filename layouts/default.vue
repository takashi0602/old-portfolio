<template>
  <div>
    <profile-header />
    <nuxt class="m-padding__top" />
  </div>
</template>

<script>
import profileHeader from "~/components/profileHeader"
export default {
  components: {
    profileHeader
  }
}
</script>

<style lang="scss">
.m-padding__top {
  padding-top: 80px;
}
</style>
