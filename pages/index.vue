<template>
  <main>
    <Content-Hero :image="hero.imageTop">
      <h3>Schlaraffia® Dusseldorpia e.V.</h3>
      <h1>
        Willkommen bei Schlaraffia Dusseldorpia
      </h1>
      <h2>Ein Verein wie sonst keiner</h2>
    </Content-Hero>
    <Content-Text-Image :image-left="intro.mainImage">
      <h3><span class="highlight">Schlaraffia</span>
        Dusseldorpia: Das sind wir
      </h3>
      <p>
        Source brings your together, in one central place. They’re easy to find and safely synced across all your
        devices—so you can access them anytime, anywhere. No more wasting the day tracking down work.
      </p>
      <div class="intro__benefits columns">
        <div class="column">
          <icon-box
            text="Ein Schlaraffe muss kein Profi sein – er hat aber Freude an Musik und Dichtkunst, an Theater und den bildenden Künsten. Auch als Amateur kann er an unseren abendlichen Treffen zur Unterhaltung der aufgeschlossenen Runde beitragen – oder einfach nur interessiert und begeistert zuhören."
            title="Interesse an Kunst"
            icon="1"/>
        </div>
        <div class="column">
          <icon-box
            text="Bei Schlaraffia darf gelacht werden! Wir haben Spaß an humorvollen Vorträgen, geistreichem Wortwitz und schlagfertigen Bemerkungen. Für Anzüglichkeiten und Zoten haben die Schlaraffen allerdings nichts übrig!"
            title="Sinn für Humor"
            icon="1"/>
        </div>
        <div class="column">
          <icon-box
            text="Wir Schlaraffen gehen freundlich und respektvoll mit einander um. Themen wie Politik, Religion und Geschäftliches sind bei unseren abendlichen Treffen tabu."
            title="Ein Herz für die Freundschaft"
            icon="1"/>
        </div>
      </div>
    </Content-Text-Image>
    <Content-Hero :image="hero.imageMiddle">
      <h3>Welche Ziele und Zwecke hat Schlaraffia</h3>
      <p style="margin-top: 1rem">
        <b>„Schlaraffia ist eine Gemeinschaft von Männern, die (…) die Pflege der Kunst und des Humors bezweckt und deren
        Hauptgrundsatz die Hochhaltung der Freundschaft ist …“</b>
        <br><br>So steht es in unserer Satzung. Abgesehen davon spielen
        in unserem Männerbund die Ehefrauen und Partnerinnen eine wichtige Rolle. Mehrmals im Jahr feiern wir mit ihnen
        zusammen und bedanken uns bei ihnen auf diese Weise für ihr Verständnis, das sie unserem vergnüglichen Spiel
        entgegenbringen. Zusätzlich treffen sich unsere Damen regelmäßig zu geselligen Runden.
      </p>
    </Content-Hero>
    <BlogSection :blog-entries="posts"/>
    <Content-Text-Image
      :enable-dots="false"
      :image-left="zitate.bildLinks"
      :image-right="zitate.bildRechts">
      <blockquote class="zitat">
        <h3>Erfahren Sie, was es mit den Schlaraffen auf sich hat</h3>
      </blockquote>
      <p>Wenn die Tage kürzer und die Nächte länger werden, treffen wir Schlaraffen in Düsseldorf uns wöchentlich am
        Freitag zu unseren gemeinsamen Abenden. Von Oktober bis Ende April darf jeder von uns, je nach Neigung und
        Talent, sich einbringen, um die Zuhörer auf unterschiedlichste Art zu unterhalten. Ob mit einer musikalischen
        Darbietung, mit einem Gedicht oder mit heiteren bis besinnlichen Gedanken in Versen oder in Prosa. Erlaubt ist
        was gefällt – allerdings sind Politik, Religion oder Geschäftliches bei uns gar kein Thema!
        <br><br>Das Erfolgsrezept der Schlaraffia – Kunst, Freundschaft, Humor – funktioniert schon seit mehr als 150 Jahren.
        Unsere Abende spielen sich im Rahmen eines persiflierten höfischen Zeremoniells aus dem Mittelalter ab. Dieser
        Rahmen – verbunden mit unseren Gewändern, altertümlichen Redewendungen und Umgangsformen – sorgt dafür, dass wir
        mit Beginn des schlaraffischen Spiels im Nu den Alltag und seine Sorgen vergessen und uns ganz auf das Vergnügen
        an Kunst und Humor konzentrieren können. Das begreift nur, wer es persönlich erlebt hat!
        <br><br>Die Begeisterung für das schlaraffische Spiel lebt seit der Gründung der Schlaraffia im Jahre 1859 – und das
        inzwischen weltweit. An mehr als 250 Orten in Europa, aber auch in Nord- und Südamerika, in Südafrika und selbst
        in Australien komm en die Freunde von Musik und Literatur, von Frohsinn und feinem Geist zusammen. Übrigens ist
        die Sprache der Schlaraffen seit ihrer Gründung Deutsch – überall auf der Welt.
        Das Symbol der schlaraffischen Geselligkeit ist der UHU, der seit jeher für Weisheit und augenzwinkernde Würde
        steht und dabei Ländergrenzen und Kontinente überwindet.</p>
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
      hero: {
        imageTop: require('assets/images/hero-schlaraffe.png'),
        imageMiddle: require('assets/images/ritter2.png'),
      },
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

.zitat h3 {
  font-weight: normal;
}
</style>
