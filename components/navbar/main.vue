<template>
  <div id="navbar" class="fixed w-full lg:bg-transparent bg-base-navbar">
    <nav class="items-center hidden gap-4 py-12 v-container lg:flex">
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
    </nav>

    <nav class="block w-full transition-all lg:hidden">
      <div class="px-2 mx-auto max-w-7xl sm:px-6 lg:px-8">
        <div class="relative flex items-center justify-between h-16">
          <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
            <!-- Mobile menu button-->
            <button
              type="button"
              class="inline-flex items-center justify-center p-2 text-white transition-all rounded-md hover:font-bold focus:outline-none"
              aria-controls="mobile-menu"
              aria-expanded="false"
              @click="toggleMenuResponsive"
            >
              <svg
                class="block w-6 h-6"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                aria-hidden="true"
                :class="{ isopen: isMobileOpen }"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16"
                />
              </svg>
            </button>
          </div>
          <div
            class="flex items-center justify-center flex-1 sm:items-stretch sm:justify-start"
          >
            <div class="flex items-center flex-shrink-0">
              <nuxt-link to="/">
                <NavbarEleLogo
                  class="transform rounded-md cursor-pointer tranform bruh-logo"
                />
              </nuxt-link>
            </div>
          </div>
        </div>
      </div>

      <div v-show="isMobileOpen" id="mobile-menu" class="sm:hidden">
        <div class="px-2 pt-2 pb-3 space-y-1">
          <nuxt-link v-for="(item, index) in items" :key="index" :to="item.to">
            <a
              href="#"
              class="block px-3 py-2 text-base font-medium text-white rounded-md "
              aria-current="page"
              @click="toggleMenuResponsive"
            >{{ item.title }}</a>
          </nuxt-link>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isMobileOpen: false,
      items: [
        {
          title: 'About me',
          to: '/about'
        },
        {
          title: 'Projects',
          to: '/projects'
        },
        {
          title: 'Skills',
          to: '/skills'
        }
      ]
    }
  },
  methods: {
    toggleMenuResponsive () {
      this.isMobileOpen = !this.isMobileOpen
    }
  }
}
</script>

<style>
  .bruh-logo {
    transform: scale(0.8);
  }
</style>
