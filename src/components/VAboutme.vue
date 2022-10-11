<template lang="pug">
  #fh5co-about.animate-box
    .container
      .row
        div(class="col-md-8 col-md-offset-2 text-center fh5co-heading")
          h2 About Me
      .row
        .col-md-6
          ul.info
            li
              span.first-block Full Name:
              span.second-block 櫻木 健太
            li
              span.first-block Github Repository:
              span.second-block https://xn--y8jl2j1b.com/
        .col-md-6
          p 
            |私は開発現場ではたらくことでユーザーやユーザーと関わりがある方々のお力になり、微力ながら社会貢献をしたいと考えています。
            br
            |現職では、スマホ販売や関連サービスの提案、お客様のお悩み解決を主に業務を行っていますが、今のやり方では目の前のお客様のお悩み解決にとどまってしまいます。
            br
            |また、現在はたいらいているお店の来客者様で5割以上のの方々が操作方法がわからないとお悩みを抱えており、更にはスタッフもお悩み解決の応対で追われてしまっているのが事実です。
            br
            |これは私が勤務しているお店だけで起こっているわけではなく、他店舗、他業種でも同じことが起こっています。
            br
            |なので私が開発現場から、その様な困っている方々に少しでも便利でわかりやすいサービス、もしくはユーザーから求められているものを開発、提供することで、少しでも社会貢献をしたいと考えています。
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class VAboutme extends Vue {
}
</script>
<style lang="scss" scoped>
.col-md-6{
  p{
    text-align: left;
  }
}
.info{
  width: 100%;
}
</style>
