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
          to: 'https://www.facebook.com/varkaria'
        },
        {
          name: 'Github',
          icon: 'github',
          to: 'https://github.com/varkaria'
        },
        {
          name: 'Fiverr',
          icon: 'fiverr',
          to: 'https://www.fiverr.com/varkaria'
        },
        {
          name: 'Spotify',
          icon: 'spotify',
          to: 'https://open.spotify.com/user/bmquj3y7m162v7vqtsbw4zxj8?si=8df13610ec0d4d8f'
        }
      ]
    }
  }
}
</script>
