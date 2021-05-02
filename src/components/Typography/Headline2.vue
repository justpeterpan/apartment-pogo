<template>
  <h2 class="text-2xl font-bold my-6">{{ text }}</h2>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: false,
      default: () => '',
    },
  },
}
</script>
