<template>
  <section class="section">
    <div class="news container is-fullhd px-4">
      <h2>Neuigkeiten aus dem Reyche der Dusseldorpen</h2>
      <div class="blog">
        <p>
        </p>
<!--        <BlogTeaser v-for="(post, index) of blogEntries" :key="index" :post="post"/>-->
      </div>
      <div class="readMore">
        <NuxtLink class="btn button px-4" to="blog">Alle Neuigkeiten ansehen</NuxtLink>
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

  h2 {
    text-align: center;
  }

  .blog {
    max-width: 1024px;
    margin: 2rem auto 0;
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-between;

    @media (max-width: 768px) {
      flex-direction: column;
      flex-wrap: nowrap;
    }

    .teaser {
      width: 30%;
      flex-basis: 30%;

      @media (max-width: 768px) {
        width: 100%;
        flex-basis: 100%;
        margin-bottom: 2rem;
      }
    }
  }

  .readMore {
    margin-top: 3rem;
    text-align: center;
  }
}
</style>
