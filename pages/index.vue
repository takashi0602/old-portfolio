<template>
  <div>
    <div class="c-container">
      <div class="mb-4">
        <div class="c-image" />
      </div>
      <div class="m-name">
        <span class="m-name__ta">た</span>
        <span class="m-name__ka">か</span>
        <span class="m-name__shi">し</span>
      </div>
      <p class="m-profile__text">
        中学生の時にドラマの影響でIT業界に興味を持ち始め、情報系の高校へ進学。<br>
        高校の卒業課題でUnityを使用し、2D格闘ゲームを作成するも、データ紛失。<br>
        セキュリティに興味を持ち、IT系の専門学校へ進学。<br>
        進学するも、Web業界へ興味を持ち、Web制作会社でアルバイトを始める。
      </p>
      <h3 class="c-subTitle">プロフィール</h3>
      <profile-list :lists="lists" class="mb-5" />
    </div>
  </div>
</template>

<script>
import profileList from "~/components/profileList"

export default {
  layouts: "default",
  components: {
    profileList
  },
  data() {
    return {
      lists: [
        {
          name: "生年月日",
          detail: "1998/06/02"
        },
        {
          name: "性別",
          detail: "男"
        },
        {
          name: "趣味",
          detail: "音楽を聴く, ギター"
        },
        {
          name: "好きな食べ物",
          detail: "メロン, お寿司, ちくわ"
        },
        {
          name: "資格",
          detail: "基本情報技術者試験"
        },
        {
          name: "技術",
          detail: "JavaScript, Vue.js, Nuxt.js, PHP, Laravel"
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "~/assets/scss/foundation/mixin.scss";
@import "~/assets/scss/foundation/variable.scss";

.c-image {
  width: 200px;
  height: 200px;
  margin: 0 auto;
  background-image: url("../assets/images/takashi.png");
  border: 5px solid $green;
  border-radius: 50%;
  @include desktop() {
    width: 250px;
    height: 250px;
  }
}

.m-name {
  width: auto;
  text-align: center;
  font-size: 1.5rem;
  background: $green;
  margin: 0 auto 30px auto;
  @include desktop() {
    width: 50%;
    font-size: 1.8rem;
  }
  &__ka {
    padding: 0 1rem;
  }
}

.m-profile {
  &__text {
    text-align: center;
    font-size: 0.8rem;
    margin-bottom: 50px;
    @include desktop() {
      font-size: 1rem;
    }
  }
}

.c-subTitle {
  margin-bottom: 15px;
}
</style>
