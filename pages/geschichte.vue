<template>
  <div>
    <Layout-HeaderPart>
      Gesellschaft "Schlaraffia ® " Dusseldorpia e.V.
      <template #overline>
        Die Entstehung
      </template>
    </Layout-HeaderPart>
    <main class="main">
      <section class="section">
        <div class="container px-4">
          <Layout-LeftRightText columns="1">
            <template #title>Die Geschichte der Dusseldorpia</template>
            Gegründet 1883 [3. im Windmond a.U. 24], sind wir Dusseldorpen eines der älteren von über 270 "Reychen" im
            heute weltweiten Verband der "Schlaraffia ® ". Von Oktober bis April treffen wir uns jeweils freitags [Glock
            7 ½ d.A.], um gemäß unserem Motto "In arte voluptas" - In der Kunst liegt das Vergnügen - mit Vorträgen und
            Musik für ein paar Stunden dem Alltag - der "Profanei" - zu entfliehen.
            Das geschieht mit viel Humor, nicht zuletzt durch die spielerische Anlehnung an höfische Sitten und
            Gebräuche des Mittelalters.<br><br>
            Unser Reych Schlaraffia Dusseldorpia hat ca. 50 Mitglieder, der Dachverband der Schlaraffia ® weltweit über
            10.000. Was diese – Männern vorbehaltene – Gemeinschaft eint, ist das gemeinsame Vergnügen an einer
            spielerischen, geistvollen Atmosphäre. Deshalb sind an unseren Abenden Alltagsthemen wie Politik, Religion
            oder Geschäfte kein Thema.<br><br>
            Auch in den Sommermonaten sind wir nicht untätig. Wir treffen uns einmal im Monat gemeinsam mit unseren
            Frauen zu einem kulturellen Programm mit anschließendem geselligem Beisammensein..<br><br>
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
