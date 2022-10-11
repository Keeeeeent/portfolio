<template lang="pug">
  #about
    VResume
    VWork
    VFooter
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import VResume from "@/components/VResume.vue";
import VWork from "@/components/VWork.vue";
import VFooter from "@/components/VFooter.vue";


@Component({
  components: {
    VResume, 
    VWork,
    VFooter,
  },
})
export default class AboutView extends Vue {}
</script>