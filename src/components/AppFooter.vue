<template>
  <footer>
    <div class="footer f-bet">
      <app-footer-button
        :selected="1 == selected"
        icon="1"
        text="ホーム"
        iconPath="./img/footer__matching.svg#home"
        @my-click="toHome"
      />
      <app-footer-button
        :selected="2 == selected"
        icon="2"
        text="マッチング"
        iconPath="./img/footer__matching.svg"
        @my-click="toMatching"
      />
      <app-footer-button
        :selected="3 == selected"
        icon="3"
        text="通知"
        iconPath="./img/footer__notification.svg"
        @my-click="toNotification"
      />
      <app-footer-button
        :selected="4 == selected"
        icon="4"
        text="マイページ"
        iconPath="./img/footer__mypage.svg"
        @my-click="toMypage"
      />
    </div>
  </footer>
</template>

<script>
import AppFooterButton from "./AppFooterButton.vue";
export default {
  components: { AppFooterButton },
  methods: {
    toHome() {
      this.$router.push({ path: "/" });
    },
    toMatching() {
      this.$router.push({ path: "/Matching" });
    },
    toNotification() {
      this.$router.push({ path: "/Notification" });
    },
    toMypage() {
      this.$router.push({ path: "/Mypage" });
    },
  },
  props: {
    text: {
      type: String,
      default: "text is not defined",
    },
    selected: {
      type: Number,
      default: -1,
    },
  },
};
</script>

<style lang="scss" scoped>
footer {
  height: 80px;
  width: 100%;
  max-width: 414px;
  box-shadow: 0px -2px 0 #d6d6d6;
  position: fixed;
  z-index: 1000;
  bottom: 0;
  background-color: #fff;
}
.footer {
  margin: auto;
  width: 343px;
}
</style>
