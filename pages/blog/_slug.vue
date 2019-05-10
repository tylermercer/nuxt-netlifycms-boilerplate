<template lang="html">
  <div class="post">
    <h1>{{title}}</h1>
    <p class="date">Posted by {{author}} on {{date}}</p>
    <div v-html="$md.render(body)"/>
  </div>
</template>

<script>
export default {
  async asyncData({ params, app, payload, route, store }) {
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
.date {
  color: darkgray;
}
.post {
  max-width: 400px;
  margin-left: auto;
  margin-right: auto;
  margin-top: 20px;
  background-color: whitesmoke;
  padding: 20px;
}
</style>
