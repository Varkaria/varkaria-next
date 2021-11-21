<template>
  <div id="home" class="h-full">
    <HomeTextanimation class="absolute bottom-0 left-0 rotate" />

    <div class="flex items-center h-full">
      <div id="title" class="font-semibold">
        <h1
          v-anime="{
            opacity: [0, 1],
            duration: 200,
            easing: 'linear'
          }"
          class="title-text"
        >
          Hello
        </h1>
        <h2
          v-anime="{
            opacity: [0, 1],
            duration: 200,
            delay: 200,
            easing: 'linear'
          }"
          class="text-2xl"
        >
          Pavaresorn Malai
        </h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.rotate {
  transform: rotate(312deg);
}

.title-text {
  font-size: 8rem;
  line-height: 9rem;
}
</style>
