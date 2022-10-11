<template>
  <div class="col-md-4 text-center">
    <div class="feature-left">
      <span class="icon">
        <i :class="icon"></i>
      </span>
      <div class="feature-copy">
        <h3>{{ title }}</h3>
        <p>
          {{ text }}
        </p>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class TextContner extends Vue {
  @Prop({ type: String, required: true })
  private icon!: string;
  @Prop({ type: String, required: true })
  private title!: string;
  @Prop({ type: String, required: true })
  private text!: string;
}
</script>
