<template lang="pug">
  #fh5co-skills.animate-box
    .container
      .row
        div(class="col-md-8 col-md-offset-2 text-center fh5co-heading")
          h2 Skills
      div(class="row row-pb-md")
        div(class="col-md-3 col-sm-6 col-xs-12 text-center" v-for="(item,index) in itemlists" :key="index")
          div(class="chart" :data-percent="item.num")
            span
              strong {{ item.title }}
              |{{ item.num }}%
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class VSkills extends Vue {
  private itemlists:{title:string,num:number}[] = [
    {title:"HTML5",num:20},
    {title:"PUG",num:10},
    {title:"CSS3",num:10},
    {title:"SASS/SCSS",num:10},
    {title:"Bootstrap",num:10},
    {title:"JavaScript",num:20},
    {title:"TypeScript",num:15},
    {title:"VueJS",num:10},
  ]
}
</script>
