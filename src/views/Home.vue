<template>
  <div class="home">
    <iframe class="avatar-test" :src="url"
    allow="geolocation; microphone; camera; midi; encrypted-media;"
    frameborder="0"></iframe>
  </div>
</template>

<script>
export default {
  data () {
    return {
      id: '7UQ4GRy0FTJcjXlxFeIQ',
      url: 'https://room.metaspace.place/user/conf?id='
    }
  },
  methods: {
    getUrl () {
      const id = this.$route.params.id
      console.log('id', id)
      if (id !== '7UQ4GRy0FTJcjXlxFeIQ') {
        // this.id =
        this.$router.push({ path: `/${id}` })
        this.url = `https://room.metaspace.place/user/conf?id=${id}`
        console.log('url', this.url)
      } else {
        this.url = `https://room.metaspace.place/user/conf?id=${this.id}`
      }
    }
  },
  mounted () {
    this.getUrl()
    console.log('11', this.$route)
  }
}
</script>

<style lang="scss" scoped>
.avatar-test {
  display: block;
  width: 100%;
  height: 100vh;
}
</style>
