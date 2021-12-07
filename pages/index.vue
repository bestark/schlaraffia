<template>
  <div>
    <main>
    test
      <li v-for="post of posts" :key="post.slug">
      <NuxtLink :to="`blog/${post.slug}`">{{ post.title }}</NuxtLink>
    </li>
    </main>
  </div>
</template>

<script>
export default {
  head() {
    return {
      script: [
        { src: "https://identity.netlify.com/v1/netlify-identity-widget.js" },
      ],
    };
  },
  async asyncData({ $content }) {
    const posts = await $content("blog").fetch();

    return {
      posts,
    };
  },
};
</script>
