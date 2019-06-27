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
import windsServo2018 from "~/assets/images/winds-servo-2018.png"
import xen from "~/assets/images/xen.png"

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
          url: "https://b00kshe1f.herokuapp.com/"
        },
        {
          name: "chat mammoth",
          detail: "チャットを楽しむアプリ",
          img: chatMammoth,
          url: "https://chat-mammoth.herokuapp.com/"
        },
        {
          name: "Winds Servo 2018 Summer Edition",
          detail: "うちわを自動で扇いでくれるシステム",
          img: windsServo2018,
          url: "https://github.com/tyokinuhata/winds-servo"
        },
        {
          name: "gour.me",
          detail: "あなたに合ったグルメをレコメンドするアプリ",
          img: gourMe,
          url: "https://trusting-wescoff-c50237.netlify.com/"
        },
        {
          name: "Xen",
          detail: "座禅アプリ",
          img: xen,
          url: "https://tyokinuhata.github.io/xen/"
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
