<template lang="pug">
  #fh5co-resume.fh5co-bg-color
    .container
      div(class="row animate-box")
        div(class="col-md-8 col-md-offset-2 text-center fh5co-heading")
          h2 My Resume
      .row
        div(class="col-md-12 col-md-offset-0")
          ul.timeline
            li(class="timeline-heading text-center animate-box")
              div
                h3 職歴
            TimeLine(timlineclass="false" company="2017-2022" title="トム通信工業株式会社")
              |ドコモショップのスタッフを5年間していました。
              |会社では責任者(チーフ)として、新人スタッフの育成やスタッフ指導をしていたほか、店舗実績向上のための取り組みとして主にオペレーション改善を任されていました。
            br
            li(class="timeline-heading text-center animate-box")
              div
                h3 学歴
            TimeLine(v-for="(item, index) in TimelineUnvertedItemLists" :key="index" :company="item.company" :title="item.title" :timelineclass="index % 2 === 0") {{ item.text }}
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import TimeLine from "@/components/parts/TimeLine.vue";
type TimeLineItems = {
    company: string;
    title: string;
    text: string;
}
@Component({
  components: {
    TimeLine,
  },
})
export default class VResume extends Vue {
  private PrimarySchool= "高坂小学校";
  private JuniorHighSchool ="浦賀中学校";
  private HighSchool = "横須賀市立明光高等学校 国際学部";
  private University = "関東学院大学 国際文化学部 英語文化学科";
  public TimelineUnvertedItemLists: TimeLineItems[] = [
    {
      company: "2017/9",
      title: this.University,
      text: "中退：理由は子供ができ育てるためのお金を自分で稼ぎたかったので就職を決意",
    },
    { company: "2015/4", 
      title: this.University, 
      text: "入学" 
    },
    { company: "2015/3",
      title: this.HighSchool,
      text: "卒業"
    },
    {
      company: "2012/4",
      title: this.HighSchool,
      text: "入学：学校説明会で素敵な野球部顧問の先生と出会い入学を決意",
    },
    { company: "2012/3", 
      title: this.JuniorHighSchool, 
      text: "卒業" 
    },
    { company: "2009/4", 
      title: this.JuniorHighSchool, 
      text: "入学" 
    },
    { company: "2009/3", 
      title: this.PrimarySchool, 
      text: "卒業" 
    },
    { company: "2003/4", 
      title: this.PrimarySchool, 
      text: "入学" 
    },
  ];
}
</script>
