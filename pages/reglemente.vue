<template>
  <div>
    <Layout-HeaderPart>
      Reglemente
      <template #subline>
        Alles zu den Reglementen der Dusseldorpen
      </template>
    </Layout-HeaderPart>
    <main class="main">
      <section class="section">
        <div class="container px-4">
          <Layout-LeftRightText columns="1">
            <template #title>Reglement zum Erwerb des Tituls RHEYNSCHIFFER</template>
            Hiermit sei allen Rittern, Junkern und Knappen des ganzen Uhuversums
            kundt gegeben, dass das hohe Reych Dusseldorpia den Titul „Rheynschiffer“ all denen Sassen dediciert, die sich folgendem Reglement
            unterziehen:
            <ol>
              <li>
                Auszureiten ist in die hohen Reyche des rheinischen Sprengels:
                <ul>
                  <li>Colonia Agrippina (8)</li>
                  <li>Dusseldorpia (54)</li>
                  <li>Aquisgranum (94)</li>
                  <li>Crefeldensis (191)</li>
                  <li>Castrum Bonnense (193)</li>
                  <li>Confluentia (225)</li>
                  <li>Duisbargum (242) Gladebachum</li>
                  <li>Monachorum (252)</li>
                  <li>Castellum Novaesium (353) Porta</li>
                  <li>Arduennae (367)</li>
                  <li>Sugambbria (398)</li>
                  <li>Brucsella (418)</li>
                </ul>
                </li>
              <li>
                Ausritte zu mehr denn einem Reych an einem Uhutag sind entgegen
                diesem Reglement und bleiben ungewertet.
              </li>
              <li>
                Es wird erwartet, dass die Ausreitenden die Reyche mit eigenen
                Fechsungen beglücken.
              </li>
              <li>
                Der Titul wird erst nach schriftlicher Meldung an das Kantzlerambt
                der Dusseldorpia mit detaillierten Nachweis aller besuchten Reyche
                und der Ausrittstermine verliehen (Kopie der Einkleber oder durch
                den Kantzler des eigenen Reyches).
              </li>
              <li>
                Zur Reception der Ehrung ist ein weiterer Einritt in die Dusseldorpia
                anlässlich der alle 2 Jahrungen stattfindenden Rheynschiffersippung
                vonnöten, in der sich der Aspirant mit einer kurzen, humorigen
                Fechsung (8-Zeiler oder Kurzbericht über den Rhein, die Rheinländer,
                rheinische Städte, Kultur am Rhein o.ä.) profiliert.
              </li>
              <li>
                Titul, Urkundt und Wappen mit der fortlaufenden Nummer werden
                taxfrei dedicieret. Für eine freiwillige Zuwendung dankt die
                Dusseldorpia uhu-hertzlich. 
              </li>
              <li>
                Nach je 1 weiteren Einritt in die genannten Reyche des rheynischen
                Sprengels können die Rheynschiffer in der nächsten RheynschifferSippung den Titul:
                „Steuermann der Rheynschiffer“
                erwerben und weiter
                nach je 2 weiteren Einritten den Titul
                „Plankenschrubber“
                nach je 3 weiteren Einritten den Titul
                „Deckmaat“
                nach je 4 weiteren Einritten den Titul
                „Lotse“
                nach je 5 weiteren Einritten den Titul
                „Deckoffizier“
                nach je 6 weiteren Einritten den Titul
                „Gallionsfigur“ und
                nach je 7 weiteren Einritten den Titul
                „Klabautermann“.
              </li>
              <li>
                Nach der Verleihung eines Tituls muss mit den Ausritten neu
                begonnen werden. Frühere Ausritte werden dann nicht mehr berücksichtigt. Mehr als ein Titul wird in einer Rheynschiffer-Sippung nicht
                verliehen.
              </li>
              <li>
                In die Allschlaraffische Stammrolle soll außer dem Titul
                „Rheynschiffer“ mit der laufenden Nummer nur die jeweils letzte
                Rangerhöhung mit dem Zusatz „…der Rheynschiffer“ eingetragen
                werden.
              </li>
              <li>
                Der Kurator der Rheynschiffer, der die Idee in jeder Weise fördert,
                trägt den Titul
                „KAPITÄN ALLER RHEYNSCHIFFER“.
                Er wird in jeder Wahlschlaraffiade vom Oberschlaraffat ernannt.
              </li>
            </ol>

            <br><br>Modifizierte Ausfertigung im Wonnemond a.U.156
            <br>Das Oberschlaraffat
          </Layout-LeftRightText>
          <download-box doc-title="Reglement ansehen" dokument="/downloads/Reglement_Rheynschiffer.pdf">
            <template #title>Reglement als Download</template>
            <template #subtitle>Titul - RHEYNSCHIFFER</template>
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
