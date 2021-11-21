<template>
  <div id="page" class="relative h-screen overflow-hidden text-white">
    <NavbarMain />

    <Nuxt class="container" />
  </div>
</template>

<style>
html {
  @apply bg-base-bg;
}
.container {
  @apply px-16;
}
</style>
