<template lang="pug">
  .home
    #page
      VAboutme
      VHeader
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import VHeader from "@/components/VHeader.vue";
import VAboutme from "@/components/VAboutme.vue";

@Component({
  components: {
    VAboutme,
    VHeader,
  },
})
export default class HomeView extends Vue {}
</script>
