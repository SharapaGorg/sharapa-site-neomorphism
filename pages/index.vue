<template>
  <div class="index-container">
    <div class="index-preview" ref="indexPreview">
      <div>
        <img :src="require('@/static/f11.svg')"/>
        <span>Fullscreen mode</span>
      </div>

      <div class="start-button" @click="redirectToMain">Let`s go</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
        disclaimerIsOver : false
    }
  },
  methods: {
    async redirectToMain() {
      await this.$router.push('/main')
    }
  },
  mounted() {
    setTimeout(() => {
      this.$refs.indexPreview.style.opacity = '1'
    }, 500)

  },
}
</script>
