<template>
  <div>
    <Layout-HeaderPart>
      <template v-slot:overline>
        Hurra! Die Burgpforte ist wieder geöffnet!
      </template>
      Termine & Neuigkeiten
    </Layout-HeaderPart>
    <main class="main">
      <section class="section justify-content">
        <download-box dokument="/downloads/Sippungsfolge_uhunetz.pdf" doc-title="Sippungsfolge 163/164 ansehen">
          <template #title>Aktuelle Sippungsfolge</template>
          <template #subtitle>Unsere Veranstaltungen Winter 2022/23</template>
        </download-box>
        <download-box dokument="/downloads/VAD_A4.pdf" doc-title="Vademecum ansehen">
          <template #title>Aktuelles Vademecum</template>
          <template #subtitle>Winterung 163/164</template>
        </download-box>
        <download-box dokument="/downloads/Krystallinen_2022.pdf" doc-title="Dokument ansehen">
          <template #title>Sommer Veranstaltungen</template>
          <template #subtitle>Krystallinen - Sommerung 163</template>
        </download-box>
      </section>
      <section class="section blog">
        <BlogTeaser v-for="(post, index) of posts" :key="index" :post="post"/>
      </section>
    </main>
  </div>
</template>

<script>
import DownloadBox from "../../components/DownloadBox";

export default {
  components: {DownloadBox},
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

.section {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  column-gap: 1rem;

  &.justify-content {
    justify-content: center;
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
