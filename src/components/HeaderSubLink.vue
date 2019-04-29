<template>
  <div>
    <b-popover :target="popupID" :placement="placement" triggers="hover focus">
      <template slot="title">Content via Slots</template>
      <template v-for="headerLink in headerSubLinks">
        <b-row :key="headerLink.id">
          <template v-if="headerLink.id === titleID">
            <template v-for="mainLink in headerLink.mainLinks">
              <b-col cols="4" :key="mainLink.id">
                <b-link :href="mainLink.link" :key="mainLink.id">{{mainLink.title}}</b-link>
              </b-col>

              <b-col cols="8" :key="mainLink.id">
                <template v-for="subLink in mainLink.subLinks">
                  <b-link :href="subLink.link" :key="subLink.id">{{subLink.title}}</b-link>
                  <br :key="subLink.id">
                </template>
              </b-col>
            </template>
          </template>
        </b-row>
      </template>
    </b-popover>
  </div>
</template>

<script>
export default {
  name: "HeaderSubLink",
  props: ["titleID", "popupID"],
  data: function() {
    return {
      headerSubLinks: [
        {
          id: 1,
          mainLinks: [
            {
              id: 1,
              title: "サービス一覧",
              link: "https://www.fabercompany.co.jp/service/",
              subLinks: [
                {
                  id: 1,
                  title: "MIERUCA（ミエルカ）",
                  link: "https://mieru-ca.com/"
                },
                {
                  id: 2,
                  title: "サチコ ミエルカ",
                  link: "https://mieru-ca.com/sachiko-mieruca/"
                },
                {
                  id: 3,
                  title: "MIERUCAユーザーヒートマップ",
                  link: "https://mieru-ca.com/heatmap/"
                },
                {
                  id: 4,
                  title: "SEO施策",
                  link: "https://www.fabercompany.co.jp/service/seo/"
                },
                {
                  id: 5,
                  title: "コンテンツマーケティング",
                  link: "https://www.fabercompany.co.jp//service/contents/"
                },
                {
                  id: 6,
                  title: "コンサルティング",
                  link: "https://www.fabercompany.co.jp//service/consulting/"
                },
                {
                  id: 7,
                  title: "コンテンツマーケティング",
                  link: "https://www.fabercompany.co.jp//service/buy-and-sell/"
                },
                {
                  id: 8,
                  title: "サービスの流れ",
                  link: "https://www.fabercompany.co.jp//service/flow/"
                }
              ]
            }
          ]
        },
        {
          id: 2,
          mainLinks: [
            {
              id: 1,
              title: "優れたサービスの背景",
              link: "https://www.fabercompany.co.jp/background/",
              subLinks: [
                {
                  id: 1,
                  title: "海外遠征",
                  link: "https://www.fabercompany.co.jp/background/overseas/"
                },
                {
                  id: 2,
                  title: "研究開発体制",
                  link: "https://www.fabercompany.co.jp/background/research/"
                },
                {
                  id: 3,
                  title: "職人会議",
                  link: "https://www.fabercompany.co.jp/background/craftsman/"
                }
              ]
            }
          ]
        },
        {
          id: 3,
          mainLinks: [
            {
              id: 1,
              title: "サービス導入実績",
              link: "https://www.fabercompany.co.jp/customer/",
              subLinks: [
                {
                  id: 1,
                  title: "サービス導入実績",
                  link: "https://www.fabercompany.co.jp/customer/"
                },
                {
                  id: 2,
                  title: "サーキュレーション 様",
                  link: "https://www.fabercompany.co.jp/customer/circulation/"
                },
                {
                  id: 3,
                  title: "富士フィルム 様",
                  link: "https://www.fabercompany.co.jp/customer/fujifilm/"
                },
                {
                  id: 4,
                  title: "ヤマトフィナンシャル 様",
                  link:
                    "https://www.fabercompany.co.jp/customer/yamatofinancial/"
                },
                {
                  id: 5,
                  title: "日宣 様",
                  link: "https://www.fabercompany.co.jp/customer/nissenad/"
                },
                {
                  id: 6,
                  title: "ランスタッド 様",
                  link: "https://www.fabercompany.co.jp/customer/randstad/"
                },
                {
                  id: 7,
                  title: "ニフティ 様",
                  link: "https://www.fabercompany.co.jp/customer/nifty/"
                },
                {
                  id: 8,
                  title: "ビズリーチ 様",
                  link: "https://www.fabercompany.co.jp/customer/bizreach/"
                },
                {
                  id: 9,
                  title: "IDOM(クルマ買取販売の「ガリバー」) 様",
                  link: "https://www.fabercompany.co.jp/customer/idom/"
                },
                {
                  id: 10,
                  title: "アソビュー 様",
                  link: "https://www.fabercompany.co.jp/customer/asoview/"
                },
                {
                  id: 11,
                  title: "サイバー・バズ 様",
                  link: "https://www.fabercompany.co.jp/customer/cyber_buzz/"
                },
                {
                  id: 12,
                  title: "魚住式スピーチメソッド 様",
                  link: "https://www.fabercompany.co.jp/customer/uozumi/"
                },
                {
                  id: 13,
                  title: "常陽銀行 様",
                  link: "https://www.fabercompany.co.jp/customer/joyobank/"
                },
                {
                  id: 14,
                  title: "ドクターシーラボ 様",
                  link: "https://www.fabercompany.co.jp/customer/ci-labo/"
                },
                {
                  id: 15,
                  title: "タビオ 様",
                  link: "https://www.fabercompany.co.jp/customer/tabio/"
                },
                {
                  id: 16,
                  title: "SATORI 様",
                  link: "https://www.fabercompany.co.jp/customer/satori/"
                }
              ]
            }
          ]
        },
        {
          id: 4,
          mainLinks: [
            {
              id: 1,
              title: "ミエルカブログ",
              link: "https://mieru-ca.com/blog/",
              subLinks: []
            }
          ]
        },
        {
          id: 5,
          mainLinks: [
            {
              id: 1,
              title: "会社概要",
              link: "https://www.fabercompany.co.jp/company/",
              subLinks: [
                {
                  id: 1,
                  title: "代表取締役メッセージ",
                  link: "https://www.fabercompany.co.jp/company/coo_message/"
                },
                {
                  id: 2,
                  title: "代表取締役Founderメッセージ",
                  link: "https://www.fabercompany.co.jp/company/message/"
                },
                {
                  id: 3,
                  title: "会社概要",
                  link: "https://www.fabercompany.co.jp/company/outline/"
                },
                {
                  id: 4,
                  title: "役員紹介",
                  link: "https://www.fabercompany.co.jp/company/staff/"
                },
                {
                  id: 5,
                  title: "CIについて",
                  link: "https://www.fabercompany.co.jp/company/ci/"
                },
                {
                  id: 6,
                  title: "CSR",
                  link: "https://www.fabercompany.co.jp/company/csr/"
                }
              ]
            }
          ]
        },
        {
          id: 6,
          mainLinks: [
            {
              id: 1,
              title: "ニュース",
              link: "https://www.fabercompany.co.jp/news/",
              subLinks: [
                {
                  id: 1,
                  title: "お知らせ",
                  link: "https://www.fabercompany.co.jp/news_category/topics/"
                },
                {
                  id: 2,
                  title: "プレスリリース",
                  link:
                    "https://www.fabercompany.co.jp/news_category/press_release/"
                },
                {
                  id: 3,
                  title: "新着セミナー・講演情報",
                  link: "https://www.fabercompany.co.jp/news_category/seminar/"
                }
              ]
            },
            {
              id: 2,
              title: "インフォメーション",
              link: "https://www.fabercompany.co.jp/media/",
              subLinks: [
                {
                  id: 1,
                  title: "マスコミ・メディア掲載実績",
                  link:
                    "https://www.fabercompany.co.jp/media_category/mass_media/"
                },
                {
                  id: 2,
                  title: "セミナー・講演実績",
                  link: "https://www.fabercompany.co.jp/media_category/lecture/"
                }
              ]
            }
          ]
        },
        {
          id: 7,
          mainLinks: [
            {
              id: 1,
              title: "採用",
              link: "https://www.fabercompany.co.jp/recruit/",
              subLinks: [
                {
                  id: 1,
                  title: "どんな会社？",
                  link: "https://www.fabercompany.co.jp/recruit/about/"
                },
                {
                  id: 2,
                  title: "どんな仕事？",
                  link: "https://www.fabercompany.co.jp/recruit/work/"
                },
                {
                  id: 3,
                  title: "社員インタビュー",
                  link: "https://www.fabercompany.co.jp/recruit/interview/"
                },
                {
                  id: 4,
                  title: "新人座談会",
                  link: "https://www.fabercompany.co.jp/recruit/discussion2018/"
                },
                {
                  id: 5,
                  title: "絆を紡ぐ",
                  link: "https://www.fabercompany.co.jp/recruit/ourbonds/"
                },
                {
                  id: 6,
                  title: "キャリアパス",
                  link: "https://www.fabercompany.co.jp/recruit/career-path/"
                },
                {
                  id: 7,
                  title: "募集職種・募集要項・採用プロセス",
                  link: "https://www.fabercompany.co.jp/recruit/guidance/"
                },
                {
                  id: 8,
                  title: "エントリーフォーム",
                  link: "https://www.fabercompany.co.jp/recruit/entry/"
                },
                {
                  id: 9,
                  title: "採用活動における個人情報保護方針",
                  link: "https://www.fabercompany.co.jp/recruit/privacy/"
                }
              ]
            },
            {
              id: 2,
              title: "募集中のインターン",
              link:
                "https://www.fabercompany.co.jp/recruit/guidance/internship/",
              subLinks: [
                {
                  id: 1,
                  title: "学生インターン・アルバイト（文理不問）",
                  link:
                    "https://www.fabercompany.co.jp/recruit/guidance/internship/"
                },
                {
                  id: 2,
                  title: "20卒ビジネスコース・2daysインターンシップ※募集終了",
                  link:
                    "https://www.fabercompany.co.jp/recruit/2019internship_spring/"
                },
                {
                  id: 3,
                  title: "人工知能・言語処理インターンシップ※募集終了",
                  link: "https://mieru-ca.com/recruit/2018internship-spring/"
                }
              ]
            }
          ]
        },
        {
          id: 8,
          mainLinks: [
            {
              id: 1,
              title: "FAQ",
              link: "https://www.fabercompany.co.jp/faq/",
              subLinks: []
            }
          ]
        },
        {
          id: 9,
          mainLinks: [
            {
              id: 1,
              title: "お問い合わせフォーム",
              link: "https://www.fabercompany.co.jp/contact/",
              subLinks: []
            },
            {
              id: 2,
              title: "無料メールマガジン登録フォーム",
              link: "https://www.fabercompany.co.jp/mail-magazine/",
              subLinks: []
            }
          ]
        }
      ],
      placement: "bottomright"
    };
  }
};
</script>