<template>
  <li class="animate-box" :class="changeclass">
    <div class="timeline-badge">
      <i class="icon-graduation-cap"></i>
    </div>
    <div class="timeline-panel" style="text-align: center;">
      <div class="timeline-heading">
        <h3 class="timeline-title">{{ title }}</h3>
        <span class="company">{{ company }}</span>
      </div>
      <div class="timeline-body">
        <p>
          <slot></slot>
        </p>
      </div>
    </div>
  </li>
</template>
<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class TimelineInverted extends Vue {
  private get changeclass() {
    return {
      "timeline-inverted": !this.timelineclass,
      "timeline-unverted": this.timelineclass,
    };
  }
  @Prop({ type: String, required: true })
  private company!: string;
  @Prop({ type: String, required: true })
  private title!: string;
  @Prop({ type: Boolean})
  private timelineclass!: boolean;
}
</script>
