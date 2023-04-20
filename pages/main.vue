<template>
  <div class="index-container">
    <img :src="require('@/static/background.png')"/>
<!--    <img :src="require('@/static/arrow.svg')" class="back-arrow" @click="backToIndex"/>-->

    <div class="gpt-input-container"></div>

  </div>
</template>

<script>
export default {
  name: "main",
  methods: {
    async backToIndex() {
      await this.$router.push('/')
    }
  }
}
</script>

<style scoped>

</style>
