<template lang="html">
  <div class="main">
    <h1>Hello World!</h1>
    <p v-for="post in blogPosts"><a :href="post._path">{{post.title}}</a></p>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo,
  },
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts;
    }
  }
}
</script>

<style lang="css" scoped>
.main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
}
</style>
