<template>
  <component
    :is="iconComponent"
    role="img"
    class="inline-block"
  />
</template>

<script>
import tv from './../assets/icons/TV.vue'
import wifi from './../assets/icons/WiFi.vue'

const icons = {
  tv: tv,
  wifi: wifi,
}

export default {
  name: 'Icon',
  props: {
    name: {
      type: String,
      required: true,
      validator(value) {
        return Object.prototype.hasOwnProperty.call(icons, value)
      },
    },
  },

  computed: {
    iconComponent() {
      return icons[this.name]
    },
  },
}
</script>
