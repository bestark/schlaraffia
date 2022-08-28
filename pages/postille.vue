<template>
  <div>
    <Layout-HeaderPart>
      Hauspostille
      <template #subline>
        Unsere interne Zeytung
      </template>
    </Layout-HeaderPart>
    <main class="main">
      <section class="section">
        <div class="container px-4">
          <download-box dokument="/downloads/HP_163_164.pdf" doc-title="Postille ansehen">
            <template #title>Hauspostille 163/164</template>
          </download-box>
        </div>
      </section>
    </main>
  </div>
</template>
<script>
import DownloadBox from "../components/DownloadBox";
export default {
  components: {DownloadBox},
  data: () => ({
    bilder: {
      bildLinks: require('assets/images/burgfrau.png'),
      bildRechts: require('assets/images/ritter.png')
    }
  })
}
</script>
<style lang="scss" scoped>
.section {
  min-height: 50vh;
}
</style>
