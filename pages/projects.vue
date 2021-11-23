<template>
  <div
    id="projects"
    class="flex flex-col items-center justify-between py-32 lg:py-16 h-min-screen"
  >
    <div class="blank" />

    <div class="w-full">
      <MainTitle title="Projects" subtitle="List of my project i did it" />

      <div class="grid content-center gap-4 px-2 mt-6 lg:px-24 lg:grid-cols-3">
        <ProjectMain
          v-for="(p, index) in projects"
          :key="index"
          :title="p.title"
          :description="p.description"
          :to="p.to"
          :icon="p.icon"
        />
      </div>
    </div>

    <MainContacts class="mt-12 lg:mt-0" />
  </div>
</template>

<script>
export default {
  data () {
    return {
      projects: [
        {
          title: 'oturna',
          description:
            'a tournament frontend, management for click the circles tournament. osu!',
          to: '/',
          icon: 'github'
        },
        {
          title: 'guweb',
          description:
            'a frontend continue in gulag-web project from modern stack, gulag.',
          to: '/',
          icon: 'github'
        },
        {
          title: 'guweb-nuxt',
          description:
            'a frontend continue in gulag-web project but use Nuxt framework.',
          to: '/',
          icon: 'github'
        },
        {
          title: 'kemona',
          description: 'new website design for kemono projects. but when?',
          to: '/',
          icon: 'github'
        },
        {
          title: 'foobar2000-rpc-album',
          description: 'a rich presence for foobar2000 with album picture!',
          to: '/',
          icon: 'github'
        },
        {
          title: 'yoshima',
          description:
            'a little serious counter overlay for 4k osu!mania gamer.',
          to: '/',
          icon: 'github'
        },
        {
          title: 'kk-discord-rpc',
          description: 'a little plugin discord rich presence for Koikatsu.',
          to: '/',
          icon: 'github'
        },
        {
          title: 'bulma-hsl',
          description:
            '👽 a little framework for who want to customise color easier bulma-hsl.',
          to: '/',
          icon: 'github'
        }
      ]
    }
  },
  head: {
    title: 'Projects'
  }
}
</script>
