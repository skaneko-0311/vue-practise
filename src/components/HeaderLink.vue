<template>
  <div>
    <template v-for="headerLink in this.headerLinks">
      <template v-if="headerLink.id === titleID">
        <b-nav-item
          :href="headerLink.link"
          :key="headerLink.id"
          :id="`popup-id-${headerLink.id}`"
        >{{headerLink.title}}</b-nav-item>
          <HeaderSubLink :titleID="titleID" :popupID="`popup-id-${headerLink.id}`" :key="headerLink.id"/>
      </template>
    </template>
  </div>
</template>

<script>
import HeaderSubLink from "./HeaderSubLink.vue";
export default {
  name: "HeaderLink",
  props: ["titleID"],
  components: {
    HeaderSubLink
  },
  data: function() {
    return {
      headerLinks: [
        {
          id: 1,
          title: "サービス一覧",
          link: "https://www.fabercompany.co.jp/service/"
        },
        {
          id: 2,
          title: "優れたサービスの背景",
          link: "https://www.fabercompany.co.jp/background/"
        },
        {
          id: 3,
          title: "サービス導入実績",
          link: "https://www.fabercompany.co.jp/customer/"
        },
        { id: 4, title: "ミエルカブログ", link: "https://mieru-ca.com/blog/" },
        {
          id: 5,
          title: "会社概要",
          link: "https://www.fabercompany.co.jp/company/"
        },
        {
          id: 6,
          title: "お知らせ",
          link: "https://www.fabercompany.co.jp/news/"
        },
        {
          id: 7,
          title: "採用",
          link: "https://www.fabercompany.co.jp/recruit/"
        },
        { id: 8, title: "FAQ", link: "https://www.fabercompany.co.jp/faq/" },
        {
          id: 9,
          title: "お問い合わせ",
          link: "https://www.fabercompany.co.jp/contact/"
        }
      ],
      show: false
    };
  }
};
</script>
<style scoped>
a:hover {
  color: red;
}
</style>
