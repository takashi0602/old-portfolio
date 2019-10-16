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
          img: require("~/assets/images/bookshelf.png"),
          url: "https://b00kshe1f.herokuapp.com/"
        },
        {
          name: "chat mammoth",
          detail: "チャットを楽しむアプリ",
          img: require("~/assets/images/chat-mammoth.png"),
          url: "https://chat-mammoth.herokuapp.com/"
        },
        {
          name: "Winds Servo 2018 Summer Edition",
          detail: "うちわを自動で扇いでくれるシステム",
          img: require("~/assets/images/winds-servo-2018.png"),
          url: "https://github.com/tyokinuhata/winds-servo"
        },
        {
          name: "gour.me",
          detail: "あなたに合ったグルメをレコメンドするアプリ",
          img: require("~/assets/images/gour-me.png"),
          url: "https://trusting-wescoff-c50237.netlify.com/"
        },
        {
          name: "Xen",
          detail: "座禅アプリ",
          img: require("~/assets/images/xen.png"),
          url: "https://tyokinuhata.github.io/xen/"
        },
        {
          name: "Duel",
          detail: "喧嘩和解カードバトル",
          img: require("~/assets/images/duel.png"),
          url: "https://uyupun.github.io/duel/"
        },
        {
          name: "TAKACSS",
          detail: "CSS/CSSアニメーションまとめサイト",
          img: require("~/assets/images/dice.gif"),
          url: "https://takashi0602.github.io/takacss/"
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
