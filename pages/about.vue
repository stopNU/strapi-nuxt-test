<template>
  <div class="">
    <div>
      About
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      content: Object
    }
  },
  created(){
    //this.fetchContent();
  },
  methods: {
    async fetchContent() {
      const content = await this.$axios.$get('http://localhost:1337/home-page')
      console.log("data", content)
      this.content = content
    }
  }
}
</script>

<style scoped lang="scss">
</style>
