<template lang="html">
  <div class="main">
    <h1>Hello World!</h1>
    <div class="posts-list">
      <h2 class="posts-list-title">Posts</h2>
      <p class="post-link" v-for="post in blogPosts"><a :href="post._path">{{post.title}}</a></p>
    </div>
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
.posts-list {
  width: 400px;
  background-color: whitesmoke;
  padding: 20px;
  margin-top: 35px;
}
.post-link {
  padding-top: 10px;
  font-size: 1.2em;
}
.main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
}
</style>
