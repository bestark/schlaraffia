<template>
  <section class="section">
    <div class="news container is-fullhd px-4">
      <h2>Neuigkeiten aus dem Reyche der Dusseldorpen</h2>
      <div class="blog">
        <BlogTeaser v-for="(post, index) of blogEntries" :key="index" :post="post"/>
      </div>
      <div class="readMore">
        <NuxtLink class="btn button px-4" to="blog">Alle Beiträge</NuxtLink>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: ["blogEntries"]
};
</script>
<style lang="scss" scoped>
.news {
  padding: 4rem 0;

  .blog {
    max-width: 1024px;
    margin: 2rem auto 0;
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-between;

    .teaser {
      width: 30%;
      flex-basis: 30%;
    }
  }

  .readMore {
    margin-top: 3rem;
    text-align: center;
  }
}
</style>
