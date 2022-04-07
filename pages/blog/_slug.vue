<template>
  <div>
    <Layout-HeaderPart>
      <template v-slot:overline>
        {{post.category}}
      </template>
      {{ post.title }}
    </Layout-HeaderPart>
    <main class="main">
      <section class="section">
        <div class="container is-fullhd px-4">
          <nuxt-content :document="post"/>
        </div>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  async asyncData({$content, params, error}) {
    let post;
    try {
      post = await $content("blog", params.slug).fetch();
      // OR const article = await $content(`articles/${params.slug}`).fetch()
    } catch (e) {
      error({message: "Blog Post not found"});
    }

    return {
      post,
    };
  },
};
</script>
<style lang="scss" scoped>

.main {
  min-height: calc(100vh - 400px);
}
</style>
