<template>
  <div class="about">
    <iframe class="no-avatar" :src="url"
    frameborder="0" allowFullScreen="true"></iframe>
  </div>
</template>

<script>
export default {
  data () {
    return {
      url: 'https://room.osensetech.com/?id='
    }
  },
  methods: {
    getUrl () {
    // 辦公室id alopaSc2jVspASHAo5Kc
      console.log(this.$route)
      const id = this.$route.params.id
      this.$router.push({ path: `/noavatar/${id}` })
      if (id === 'alopaSc2jVspASHAo5Kc') {
        this.url = `https://room.osensetech.com/?id=${id}`
      } else {
        this.url = `https://room.metaspace.place/?id=${id}`
      }
      console.log(this.url)
    }
  },
  mounted () {
    this.getUrl()
  }
}
</script>

<style lang="scss" scoped>
.no-avatar {
  display: block;
  width: 100%;
  height: 100vh;
}
</style>
