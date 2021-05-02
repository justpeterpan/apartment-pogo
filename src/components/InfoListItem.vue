<template>
  <div class="flex flex-row gap-2 text-lg">
    <div>{{ icon }}</div>
    <div>{{ text }}</div>
  </div>
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
