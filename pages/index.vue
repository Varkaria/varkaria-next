<template>
  <div id="home" class="h-min-screen">
    <HomeTextanimation
      class="absolute bottom-0 left-0 hidden rotate 2xl:block"
    />

    <div class="flex flex-col justify-between py-24 h-min-screen">
      <div class="blank" />

      <div id="title" class="font-semibold">
        <h1
          v-anime="{
            opacity: [0, 1],
            duration: 200,
            easing: 'linear'
          }"
          class="text-center title-text lg:text-left"
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
          class="text-3xl text-center lg:text-left"
        >
          Pavaresorn Malai
        </h2>

        <h3
          v-anime="{
            opacity: [0, 1],
            duration: 200,
            delay: 800,
            easing: 'linear'
          }"
          class="mt-6 text-lg text-center text-gray-400 lg:text-left"
        >
          Student, Fullstack Developer, Designer
        </h3>
      </div>

      <MainContacts class="justify-center lg:justify-start" />
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Hello'
  }
}
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
