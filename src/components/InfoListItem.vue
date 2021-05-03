<template>
  <li class="flex flex-row gap-2 text-lg">
    <img :src="icon" />
    <div>{{ text }}</div>
  </li>
</template>

<script>
export default {
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
