<template>
  <div>
    <profile-header />
    <nuxt />
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
