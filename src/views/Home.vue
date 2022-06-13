<template>
  <div class="home">
    <iframe class="avatar-test" src="https://room.metaspace.place/user/conf?id=7UQ4GRy0FTJcjXlxFeIQ"
    allow="geolocation; microphone; camera; midi; encrypted-media;"
    frameborder="0"></iframe>
  </div>
</template>

<script>
export default {
  mounted () {
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
