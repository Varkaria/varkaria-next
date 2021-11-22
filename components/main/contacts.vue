<template>
  <div id="contact" class="flex gap-6 func-hidden">
    <a
      v-for="(c, index) in contacts"
      :key="index"
      class="transition-all link"
      :href="c.to"
    >
      <img
        :src="require(`~/assets/logo/contacts/${c.icon}.svg`)"
        :alt="c.name"
      >
    </a>
  </div>
</template>

<script>
export default {
  data () {
    return {
      contacts: [
        {
          name: 'Facebook',
          icon: 'facebook',
          to: 'https://www.facebook.com/'
        },
        {
          name: 'Github',
          icon: 'github',
          to: 'https://www.facebook.com/'
        },
        {
          name: 'Twitter',
          icon: 'twitter',
          to: 'https://www.facebook.com/'
        }
      ]
    }
  }
}
</script>
