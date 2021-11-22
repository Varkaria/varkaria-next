<template>
  <nuxt-link :to="to">
    <a class="px-4 text-lg font-semibold">
      {{ title }}
    </a>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    to: {
      type: String,
      required: true
    }
  }
}
</script>
