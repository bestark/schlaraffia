<template>
  <div>
    <Layout-HeaderPart>
      <template v-slot:overline>
        Hurra! Die Burgpforte ist wieder geöffnet!
      </template>
      Termine & Neuigkeiten
    </Layout-HeaderPart>
    <main class="main">
      <section class="section">
        <div class="sippung">
          <h2>Aktuelle Sippungsfolge</h2>
          <h4>Unsere Veranstaltungen Winter 2022</h4>
          <a class="button" href="/downloads/Sippungsfolge_uhunetz.pdf">Sippungsfolge 163 ansehen</a>
        </div>
      </section>
      <section class="section blog">
        <BlogTeaser v-for="(post, index) of posts" :key="index" :post="post"/>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  head() {
    return {
      script: [
        {src: "https://identity.netlify.com/v1/netlify-identity-widget.js"},
      ],
    };
  },
  async asyncData({$content}) {
    const posts = await $content("blog").fetch();

    return {
      posts,
    };
  },
};
</script>
<style lang="scss" scoped>

.main {
  min-height: calc(100vh - 400px);
}

.sippung {
  background-color: lighten($color-main-blue, 50%);
  max-width: 600px;
  border-radius: 1rem;
  padding: 2rem;
  margin: 0 auto;
  text-align: center;

  .button {
    margin-top: 2rem;
  }
}

.blog {
  margin: 0 auto;
  max-width: 1024px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-column-gap: 4rem;
  grid-row-gap: 4rem;

  @media (max-width: 768px) {
    grid-template-columns: 1fr;

    .teaser {
      margin: 0 auto;
    }
  }
}
</style>
