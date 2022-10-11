<template lang="pug">
  div
    .gototop.js-top
      a(href="#" class="js-gotop")
        i(class="icon-arrow-up22")
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class VFooter extends Vue {}
</script>
