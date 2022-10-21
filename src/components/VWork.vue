<template lang="pug">
    #fh5co-work.fh5co-bg-dark
        .container
          div(class="row animate-box")
            div(class="col-md-8 col-md-offset-2 text-center fh5co-heading")
              h2 頑張ってきたこと
          .row
            div(class="col-md-3 text-center col-padding animate-box")
              span(class="work" style="background-image: url(images/blog3.jpg);")
                .desc
                  h3 諦めない気持ち
                  span 高校野球を通して何事も取り組み、最後まで諦めない気持ちを培ってきました。
            div(class="col-md-3 text-center col-padding animate-box")
              a(href="https://xn--y8jl2j1b.com/" class="work" style="background-image: url(images/blog.jpg);")
                .desc
                  h3 さくらぼ.com
                  span 独学で得た知識をフル活用しゼロからホームページを構築し、機能改善・追加の繰り返しをしています。
            div(class="col-md-3 text-center col-padding animate-box")
              span(class="work" style="background-image: url(images/blog4.jpg);")
                .desc
                  h3 責任ある立場の人間として
                  span 現職ではドコモショップ店員としてコミュケーション能力を磨くと共に、チーフとしてマネジメント力もつけることができました。
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class VWork extends Vue {}
</script>
<style lang="sass" scoped>
.work
  .desc
    span
      color: #000
</style>