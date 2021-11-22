<template>
  <a
    class="flex items-center gap-4 px-8 py-10 transition-all transform rounded-md bg-base-block hover:scale-95"
    :href="to"
  >
    <img
      :src="require(`~/assets/logo/contacts/${icon}.svg`)"
      class="w-16 h-16"
    >
    <div id="title">
      <h1 class="text-3xl font-bold text-white">
        {{ title }}
      </h1>
      <p class="text-white text-description text-opacity-60">
        {{ description }}
      </p>
    </div>
  </a>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    to: {
      type: String,
      required: false,
      default: '/'
    },
    icon: {
      type: String,
      required: false,
      default: 'github'
    }
  }
}
</script>

<style>
.text-description {
  line-height: 1.4rem;
  font-size: 1rem;
}
</style>
