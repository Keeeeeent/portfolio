<template lang="pug">
  #fh5co-features.animate-box
    .container
      .services-padding
        .row
          TextContner(v-for="(item, index) in itemlists" :key="index" :icon="item.icon" :text="item.text" :title="item.title")
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import TextContner from "@/components/parts/TextContner.vue";

@Component({
  components: {
    TextContner,
  },
})
export default class VFeatures extends Vue {
  private itemlists: { icon: string; text: string; title: string }[] = [
    {
      icon: "icon-bargraph",
      text: "WEBサイト構築のための基本的な知識だけでなく、SEO・解析ツール・サーバーの仕組みなどを学習しました。",
      title: "SITEBILUD",
    },
    {
      icon: "icon-genius",
      text: "JavaScriptの基本的な知識だけでなく拡張言語であるTypeScriptやフレームワーク、ライブラリ、Webpackなど周辺知識まで学習しました。",
      title: "SCRIPT",
    },
    {
      icon: "icon-search",
      text: "Pug・Sass・Scss・EmmetなどHTMLやCSSを書くためのメタ言語を学習、Bootstrap・テーマテンプレートのカスタマイズの学習をしてきました。",
      title: "HTML&CSS",
    },
  ];
}
</script>
