<template>
  <div id="navbar" class="container fixed flex items-center gap-4 py-12">
    <nuxt-link to="/">
      <NavbarEleLogo
        class="transition-all transform cursor-pointer hover:scale-105"
      />
    </nuxt-link>

    <NavbarEleItem
      v-for="(i, index) in items"
      :key="index"
      v-anime="{
        opacity: [0, 1],
        duration: 500,
        easing: 'linear',
        delay: 100 * index + 1
      }"
      :title="i.title"
      :to="i.to"
    />
  </div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          title: 'About me',
          to: '/'
        },
        {
          title: 'Projects',
          to: '/projects'
        },
        {
          title: 'Skills',
          to: '/'
        }
      ]
    }
  }
}
</script>
