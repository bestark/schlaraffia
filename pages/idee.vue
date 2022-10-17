<template>
  <div>
    <Layout-HeaderPart>
      Die Idee
      <template #subline>
        Was genau ist Schlaraffia?
      </template>
    </Layout-HeaderPart>
    <main class="main">
      <section class="section">
        <div class="container px-4">
          <Layout-LeftRightText columns="1">
            <template #title>Die Geschichte Schlaraffias</template>
            Das Erfolgsrezept der Schlaraffia – Kunst, Freundschaft, Humor – funktioniert schon seit mehr als 150
            Jahren.
            Unsere Abende spielen sich im Rahmen eines persiflierten höfischen Zeremoniells aus dem Mittelalter ab. Dieser
            Rahmen – verbunden mit unseren Gewändern, altertümlichen Redewendungen und Umgangsformen – sorgt dafür, dass wir
            mit Beginn des schlaraffischen Spiels im Nu den Alltag und seine Sorgen vergessen und uns ganz auf das Vergnügen
            an Kunst und Humor konzentrieren können. Das begreift nur, wer es persönlich erlebt hat!
            <br><br>Die Begeisterung für das schlaraffische Spiel lebt seit der Gründung der Schlaraffia im Jahre 1859 – und
            das
            inzwischen weltweit. An mehr als 250 Orten in Europa, aber auch in Nord- und Südamerika, in Südafrika und selbst
            in Australien komm en die Freunde von Musik und Literatur, von Frohsinn und feinem Geist zusammen. Übrigens ist
            die Sprache der Schlaraffen seit ihrer Gründung Deutsch – überall auf der Welt.
            Das Symbol der schlaraffischen Geselligkeit ist der UHU, der seit jeher für Weisheit und augenzwinkernde Würde
            steht und dabei Ländergrenzen und Kontinente überwindet.
          </Layout-LeftRightText>
          <Content-Text-Image
            :enable-dots="false"
            :image-left="bilder.bildLinks">
            <blockquote class="zitat">
              <h3>"Schlaraffia® ist eine Gemeinschaft von Männern, die in gleich­gesinntem Streben die Pflege der
                Kunst und des Humors bezweckt und deren Hauptgrundsatz die Hochhaltung der Freundschaft ist."
              </h3></blockquote>
            <p><b>Zitat aus der Satzung</b></p>
          </Content-Text-Image>

          <Layout-LeftRightText columns="1">
            <h3>Wie wird man Schlaraffe?</h3>
            In Schlaraffia ist nichts geheim.
            Die Burgpforte steht für jeden interessierten Mann offen, eine Anmeldung ist jedoch erforderlich; sie
            erfolgt durch z.B. telefonische Kontaktaufnahme mit dem Kanzler des Reyches, oder bei persönlicher
            Bekanntheit mit einem Schlaraffen durch diesen. Der so avisierte Gast „reytet” dann als „Pilger” ein.
            Bekleidet mit einer Pilgerhaube und wohlbetreut durch Sassen des Reyches wird er mit all dem Neuen
            Bekanntschaft schließen.<br><br>

            Wer dann Schlaraffe werden möchte, lässt sich durch einen Ritter des Reyches, der ihm als Pate zur Seite
            steht, anmelden. Über die Aufnahme entscheiden die Mitglieder des jeweiligen Reyches nach einer Phase
            gegenseitigen Kennenlernens. Als „Prüfling” wird der bisherige Pilger herausfinden, ob ihm das Spiel auf
            Dauer Freude machen wird und wie er sich aktiv einbringen kann. Ein gewichtiges Wort hat allerdings der
            weibliche Anhang des Prüflings, muss doch die designierte „Burgfrau” oder „Burgwonne” bereit sein, ihren
            „Burgherrn” in der Winterung zu den wöchentlichen Sippungen zu beurlauben. Mehrmals in der Winterung ist die
            Burgpforte aber auch für Burgfrauen, Familie und Gäste zu Veranstaltungen außerhalb des Sippungsgeschehens
            geöffnet. So entstehen freundschaftliche Kontakte zwischen den Familien der Schlaraffen.
            In der Öffentlichkeit erkennen sich Schlaraffen an einer kleinen am Revers getragenen Perle, der
            „Rolandnadel”.<br><br>

            <h3>Lulu!</h3>
          </Layout-LeftRightText>
        </div>
      </section>
    </main>
  </div>
</template>
<script>
export default {
  data: () => ({
    bilder: {
      bildLinks: require('assets/images/burgfrau.png'),
      bildRechts: require('assets/images/ritter.png')
    }
  })
}
</script>
<style lang="scss" scoped>
</style>
