<template>
  <div
    v-show="!isLoading"
    id="page"
    class="relative overflow-hidden text-white h-min-screen"
  >
    <transition
      enter-active-class="transition duration-1000 ease-out delay-500"
      enter-class="transform scale-95 opacity-0"
      enter-to-class="transform scale-100 opacity-100"
    >
      <div v-show="!isLoading" id="main" class="h-min-screen">
        <NavbarMain class="z-10" />
        <Nuxt class="z-0 v-container" />
      </div>
    </transition>

    <transition
      leave-active-class="transition ease-in duration-250"
      leave-class="transform scale-100 opacity-100"
      leave-to-class="transform opacity-0 scale-80"
    >
      <div
        v-show="isLoading"
        id="loading-screen"
        class="absolute top-0 flex items-center justify-center w-screen h-screen z-60"
      >
        <svg
          class="w-12 h-12 text-white animate-spin"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
        >
          <circle
            class="opacity-25"
            cx="12"
            cy="12"
            r="10"
            stroke="currentColor"
            stroke-width="4"
          />
          <path
            class="opacity-75"
            fill="currentColor"
            d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"
          />
        </svg>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isLoading: true
    }
  },
  mounted () {
    this.isLoading = false
  }
}
</script>

<style>
html {
  @apply bg-base-bg;
}
.v-container {
  @apply px-6 lg:px-16;
}
.h-min-screen {
  min-height: 100vh;
}
</style>
