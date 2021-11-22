<template>
  <div id="home" class="h-min-screen">
    <HomeTextanimation
      class="absolute bottom-0 left-0 hidden rotate 2xl:block"
    />

    <div class="flex flex-col justify-between h-min-screen py-24">
      <div class="blank" />

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
          class="text-3xl"
        >
          Pavaresorn Malai
        </h2>
      </div>

      <MainContacts />
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
  font-size: 10rem;
    line-height: 11rem;
}
</style>
