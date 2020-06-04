<template>
  <div class="container">
    <div>
      test
      <!--<LazyHomepageHeader :data="content.header" v-if="content.header" />
      <LazyHomepageIntro :data="content.intro" v-if="content.intro" />
      <LazyHomepageFeatures :data="content.features" v-if="content.features" />
      <LazyHomepageSpecialProject :data="content.special_project" v-if="content.special_project" />
      <LazyHomepageFeaturedArticles />-->
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      content: Object,
    }
  },
  created(){
    this.fetchContent();
    
  },
  mounted(){
    //console.log('baseAPIUrl', process.env.baseAPIUrl) // world
  },
  methods: {
    async fetchContent() {
      const content = await this.$axios.$get(process.env.baseAPIUrl + 'home-page')
      console.log("data", content)
      this.content = content
    }
  }
}
</script>

<style scoped lang="scss">
</style>
