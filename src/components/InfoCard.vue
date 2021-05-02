<template>
  <div class="max-w-max max-h-max rounded-2xl border">
    <div class="m-4">
      <div class="mb-2">{{ icon }}</div>
      <div class="font-bold text-xl">{{ title }}</div>
      <div class="text-lg">{{ details }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    details: {
      type: String,
      required: true,
    },
  },
}
</script>

<style></style>
