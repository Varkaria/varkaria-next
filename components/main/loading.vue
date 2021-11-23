<template>
  <div>
    <transition name="fade">
      <div
        v-if="loading"
        class="absolute z-10 px-6 py-4 rounded-lg right-4 bottom-4"
      >
        <h1
          class="flex items-center justify-center text-xs font-semibold text-white "
        >
          <svg
            class="w-8 h-8 text-white animate-spin"
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
        </h1>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  transition: 'fade',
  data: () => ({
    loading: false
  }),
  methods: {
    start () {
      this.loading = true
    },
    finish () {
      this.loading = false
    }
  }
}
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.25s ease-in-out, transform 0.25s ease-in-out;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
