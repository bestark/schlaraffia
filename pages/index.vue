<template>
  <main>
    <Content-Hero />
    <Content-Text-Image :image-left="intro.mainImage">
      <h3>Das sind die <span class="highlight">Schlaraffen</span> Dusselorpia</h3>
      <p>
        Source brings your together, in one central place. They’re easy to find and safely synced across all your
        devices—so you can access them anytime, anywhere. No more wasting the day tracking down work.
      </p>
      <div class="intro__benefits columns">
        <div class="column">
          <icon-box text="Source brings your together, in one central place." title="Vergnügen an der Kunst"
                    icon="1"/>
        </div>
        <div class="column">
          <icon-box text="Source brings your together, in one central place." title="Humor" icon="1"/>
        </div>
        <div class="column">
          <icon-box text="Source brings your together, in one central place." title="Freundschaft" icon="1"/>
        </div>
      </div>
    </Content-Text-Image>
    <Content-Hero />
    <Content-Text-Image
      :enable-dots="false"
      :image-left="zitate.bildLinks"
      :image-right="zitate.bildRechts">
      <blockquote class="zitat"><h3>"Schlaraffia® ist eine Gemeinschaft von Männern, die in gleich­gesinntem Streben die Pflege der
        Kunst und des Humors bezweckt und deren Hauptgrundsatz die Hochhaltung der Freundschaft ist."
      </h3></blockquote>
      <p><b>Zitat aus der Satzung</b></p>
    </Content-Text-Image>
  </main>
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
  data() {
    return {
      zitate: {
        bildLinks: require('assets/images/burgfrau.png'),
        bildRechts: require('assets/images/ritter.png')
      },
      intro: {
        mainImage: require('assets/images/knappe.png')
      }
    }
  }
};
</script>
<style lang="scss" scoped>

.zitat h3{
  font-weight: normal;
}

</style>
