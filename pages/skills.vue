<template>
  <div
    id="skills"
    class="flex flex-col items-center justify-between py-32 lg:py-16 h-min-screen"
  >
    <div class="blank" />

    <div class="w-full">
      <MainTitle
        title="Skills"
        subtitle="List of my language, library, framework i can do it"
      />

      <div class="grid gap-4 px-4 mt-6 xl:px-64">
        <div
          v-for="(sk, index) in skills"
          :key="index"
          class="grid justify-center gap-5 lg:gap-6 lg:flex"
        >
          <div
            v-for="(s, index2) in sk"
            :key="index2"
            class="flex items-center justify-center gap-4 px-8 py-4 rounded-md bg-base-block"
          >
            <i :class="`text-4xl lg:text-5xl icon-${s.icon}`" />
            <h1 class="text-xl font-bold lg:text-3xl">
              {{ s.title }}
            </h1>
          </div>
        </div>
      </div>
    </div>

    <MainContacts class="mt-12 lg:mt-0" />
  </div>
</template>

<script>
export default {
  data () {
    return {
      skills: [
        [
          {
            icon: 'python',
            title: 'Python'
          },
          {
            icon: 'javascript',
            title: 'Javascript'
          },
          {
            icon: 'html',
            title: 'HTML'
          },
          {
            icon: 'css',
            title: 'CSS'
          }
        ],
        [
          {
            icon: 'tailwindcss',
            title: 'TailwindCSS'
          },
          {
            icon: 'windicss',
            title: 'WindiCSS'
          }
        ],
        [
          {
            icon: 'nuxt',
            title: 'Nuxt.js / Vue.js'
          },
          {
            icon: 'node',
            title: 'Node.js'
          }
        ],
        [
          {
            icon: 'flask',
            title: 'Flask / Quart'
          }
        ]
      ]
    }
  },
  head: {
    title: 'Skills'
  }
}
</script>
