<template>
  <ul v-for="(item, index) of items" :key="index">
    <InfoListItem :icon="item.icon" :text="item.feature" />
  </ul>
</template>

<script>
import InfoListItem from './InfoListItem.vue'

export default {
  components: { InfoListItem },
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
}
</script>
