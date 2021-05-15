<template>
  <h2 class="text-xl md:text-2xl font-semibold md:font-bold">
    {{ text }}
  </h2>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true,
    },
  },
}
</script>
