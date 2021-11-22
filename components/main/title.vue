<template>
  <div>
    <h1 class="text-6xl font-semibold text-center uppercase">
      {{ title }}
    </h1>
    <h2 class="mt-2 text-xl font-semibold text-center text-white text-opacity-60">
      {{ subtitle }}
    </h2>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    subtitle: {
      type: String,
      required: true
    }
  }
}
</script>
