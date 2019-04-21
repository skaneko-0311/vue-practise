<template>
  <div>
    <a href>
      <img src="../assets/company_logo.png">
    </a>
    <ol v-for="menu in menus" :key="menu.id" v-html="makeHeaderLinks(menu)"></ol>
  </div>
</template>

<script>
export default {
  name: "MyHeader",
  data: function() {
    return {
      menus: [
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
      ]
    };
  },
  methods: {
    makeHeaderLinks: function(menu) {
      let out = '<a href="' + menu.link + '">' + menu.title + "</a>";
      return out;
    }
  }
};
</script>

<style scoped>
ol {
  display: inline-block;
}
img:hover {
  opacity: 0.5;
  -webkit-transition: 0s;
  transition: 0s;
}
</style>
