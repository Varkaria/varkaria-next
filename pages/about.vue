<template>
  <div
    id="about"
    class="flex flex-col items-center justify-between py-32 h-min-screen"
  >
    <div class="blank" />

    <div>
      <MainTitle title="About me" subtitle="My infomation" />

      <img class="mx-auto mt-8" :src="require(`~/assets/image/profile.png`)">

      <h2 class="max-w-2xl mx-auto mt-6 text-xl font-medium text-center text-white">
        👋 Hello everyone. My name is Pavaresorn Malai a.k.a. Varkaria. I'm 17 years old from
        Thailand. Nice to meet you everyone!!
      </h2>

      <h2 class="max-w-3xl mt-6 text-lg font-semibold text-center text-white text-opacity-60">
        I love to code, design, playing games such as VRchat, Quaver and osu!.
        I'm also Interest in Programing, Designing, Motion Graphic and anything
        I want to do
      </h2>
    </div>

    <MainContacts class="mt-12 lg:mt-0" />
  </div>
</template>

<script>
export default {
  head: {
    title: 'About me'
  }
}
</script>
