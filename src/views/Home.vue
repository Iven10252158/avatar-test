<template>
  <div class="home">
    <iframe class="avatar-test" :src="url"
    allow="geolocation; microphone; camera; midi; encrypted-media; allowFullScreen; allowtransparency"
    allowFullScreen="true" allowtransparency="true" scrolling="no"
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
.home {
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    overflow-y: hidden;
    -webkit-overflow-scrolling: touch;
  .avatar-test {
    display: block;
    width: 100%;
    height: 100%;
  }
}
</style>
