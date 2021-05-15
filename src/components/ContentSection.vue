<template>
  <div class="m-10">
    <div class="flex">
      <headline-2 :text="title" class="flex-1" />
      <slot name="avatar" />
    </div>
    <slot name="content" />
    <hr class="mt-8 md:mt-14" />
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
