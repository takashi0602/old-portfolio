<template>
  <div>
    <div class="c-container">
      <h3 class="c-subTitle">作品</h3>
      <product-list :lists="products" />
    </div>
  </div>
</template>

<script>
import productList from "~/components/productList"
import bookshelf from "~/assets/images/bookshelf.png"
import chatMammoth from "~/assets/images/chat-mammoth.png"
import gourMe from "~/assets/images/gour-me.png"

export default {
  layouts: "default",
  components: {
    productList
  },
  data() {
    return {
      products: [
        {
          name: "Bookshelf",
          detail: "本を管理するためのアプリ",
          img: bookshelf,
        },
        {
          name: "chat mammoth",
          detail: "チャットを楽しむアプリ",
          img: chatMammoth,
        },
        {
          name: "gour.me",
          detail: "あなたに合ったグルメをレコメンドするアプリ",
          img: gourMe,
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.c-container {
  padding-top: 20px;
}

.c-subTitle {
  margin-bottom: 20px;
}
</style>
