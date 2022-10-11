<template lang="pug">
     header(id="fh5co-header" class="fh5co-cover js-fullheight" role="banner" style="background-image:url(images/cover_bg_3.jpg);" data-stellar-background-ratio="0.5")
        .overlay
        .container
          .row
            div(class="col-md-8 col-md-offset-2 text-center")
              div(class="display-t js-fullheight")
                div(class="display-tc js-fullheight animate-box" data-animate-effect="fadeIn")
                  div(class="profile-thumb" style="background: url(images/0004.png);")
                  h1
                    span Sakuragi Kenta
                  h3
                    span Web Developer
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class VHeader extends Vue {}
</script>