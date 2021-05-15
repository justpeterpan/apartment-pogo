<template>
  <li
    v-if="!detailView"
    class="grid grid-cols-2 md:flex md:flex-row gap-2 my-2 md:my-0 text-lg"
  >
    <div class="md:order-last">{{ text }}</div>
    <Icon :name="icon" class="justify-self-end md:order-first" />
  </li>
  <li v-else class="grid grid-rows-3 grid-flow-col">
    <Icon :name="icon" class="row-span-3" />
    <div class="font-bold text-lg col-span-2">{{ title }}</div>
    <div class="row-span-2 col-span-2">{{ text }}</div>
  </li>
</template>

<script>
import Icon from '../Icon.vue'

export default {
  name: 'InfoListItem',
  components: { Icon },
  props: {
    detailView: {
      type: Boolean,
      required: true,
    },
    icon: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: false,
    },
  },
}
</script>
