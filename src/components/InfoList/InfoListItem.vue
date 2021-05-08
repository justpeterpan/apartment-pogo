<template>
  <li class="flex flex-row gap-2 text-lg">
    <Icon :name="icon" />
    <div>{{ text }}</div>
  </li>
</template>

<script>
import Icon from '../Icon.vue'

export default {
  name: 'InfoListItem',
  components: { Icon },
  props: {
    icon: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
  },
}
</script>
