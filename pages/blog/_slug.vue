<template lang="html">
  <div class="post">
    <h1>{{title}}</h1>
    <p class="date">Posted by {{author}} on {{date}}</p>
    <div class="post-content" v-html="$md.render(body)"/>
    <p class="back-link"><n-link to="/">Back</n-link></p>
  </div>
</template>

<script>
export default {
  async asyncData({ params, app, payload, route, store }) {
    /*
    Interestingly, if you just return the raw post object as it is imported,
    Nuxt fails to build, but if you create your own object with the data you
    need, it works. The issue is discussed here, but apparently it wasn't
    completely fixed. https://github.com/nuxt-community/apollo-module/issues/163
    However, I like the code more this way anyway--it's more explicit what
    you're bringing in from the JSON.
    */
    let post = await import(`~/content/blog/${params.slug}.json`);
    return {
      date: post.date,
      body: post.body,
      title: post.title,
      author: post.author,
    };
  }
}
</script>

<style lang="css" scoped>
.back-link, .date, .post-content {
  padding-top: 10px;
}

.date {
  color: darkgray;
}
.post {
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
  margin-top: 20px;
  background-color: whitesmoke;
  padding: 20px;
}
</style>
