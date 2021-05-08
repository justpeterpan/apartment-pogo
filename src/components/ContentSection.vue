<template>
  <div class="m-10">
    <headline-2 :text="title" />
    <slot name="content"></slot>
    <hr class="mt-14" />
  </div>
</template>

<script>
import Headline2 from './Typography/Headline2.vue'

export default {
  components: {
    Headline2,
  },
  props: {
    title: {
      type: String,
      required: false,
      default: () => '',
    },
  },
}
</script>
