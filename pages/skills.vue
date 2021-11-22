<template>
  <div
    id="skills"
    class="flex flex-col items-center justify-between py-16 h-min-screen"
  >
    <div class="blank" />

    <div class="w-full">
      <MainTitle
        title="Skills"
        subtitle="List of my language, library, framework i can do it"
      />

      <div class="grid gap-4 px-4 mt-12 xl:px-64">
        <div
          v-for="(sk, index) in skills"
          :key="index"
          class="grid justify-center gap-5 my-4 lg:gap-24 lg:flex"
        >
          <div v-for="(s, index) in sk" :key="index" class="flex items-center justify-center gap-6">
            <img
              :src="require(`~/assets/icons/${s.icon}.svg`)"
              class="w-8 h-8 lg:w-20 lg:h-20"
            > <h1 class="text-xl font-bold lg:text-3xl">{{ s.title }}</h1>
          </div>
        </div>
      </div>
    </div>

    <MainContacts />
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
  }
}
</script>
