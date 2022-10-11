<template lang="pug">
    #skill
      VSkills
      VFeatures
      VFooter
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import VSkills from "@/components/VSkills.vue";
import VFooter from "@/components/VFooter.vue";
import VFeatures from "@/components/VFeatures.vue"  

@Component({
  components: {
    VSkills,
    VFeatures,
    VFooter,
  },
})
export default class SkillView extends Vue {}
</script>
