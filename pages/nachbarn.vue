<template>
  <div>
    <Layout-HeaderPart>
      Unsere Nachbarn
    </Layout-HeaderPart>
    <main class="main">
      <section class="section">
        <div class="container is-fullhd px-4">
          <Layout-LeftRightText>
            <template #title>Verweise zu Nachbar-Reychen</template>
          </Layout-LeftRightText>
        </div>
        <div class="container nachbarn is-fullhd px-4">
          <a :href="reych.url" target="_blank" class="reych" v-for="reych of reyche" :key="reyche.nummer">
            <img :src="reych.logo" />
              <div class="reych__content">
                {{reych.name}} {{reych.nummer}}
                <div class="reych__city">{{reych.stadt}}</div>
              </div>
          </a>
        </div>
      </section>
    </main>
  </div>
</template>
<script>
const alleNachbarn = [
  {
    name: 'Colonia Agrippina',
    logo: require('assets/images/reyche/colonia.jpg'),
    stadt: 'Köln',
    nummer: '(8)',
    url: 'http://www.schlaraffia-colonia-agrippina.de'
  },
  {
    name: 'Elberfeldensis',
    logo: require('assets/images/reyche/elberfeldensis.jpg'),
    stadt: 'Wuppertal',
    nummer: '(34)',
    url: 'http://www.elberfeldensis.de'
  },
  // {
  //   name: 'Assindia',
  //   logo: require('assets/images/reyche/assindia.jpg'),
  //   stadt: '',
  //   nummer: '(50)',
  //   url: 'http://www.schlaraffia-assindia.org'
  // },
  {
    name: 'Aquisgranum',
    logo: require('assets/images/reyche/aquisgranum.jpg'),
    stadt: 'Aachen',
    nummer: '(94)',
    url: 'http://www.aquisgranum.de'
  },
  {
    name: 'Bochumensis',
    logo: require('assets/images/reyche/bochumensis.jpg'),
    stadt: 'Bochum',
    nummer: '(166)',
    url: 'http://www.bochumensis.de'
  },
  {
    name: 'Truymannia',
    logo: require('assets/images/reyche/truymannia.jpg'),
    stadt: 'Dortmund',
    nummer: '(177)',
    url: 'http://www.truymannia.de'
  },
  {
    name: 'Hagena',
    logo: require('assets/images/reyche/hagena.jpg'),
    stadt: 'Hagen',
    nummer: '(189)',
    url: 'http://www.schlaraffia-hagena.de'
  },
  {
    name: 'Crefeldensis',
    logo: require('assets/images/reyche/crefeldensis.jpg'),
    stadt: 'Krefeld',
    nummer: '(191)',
    url: 'http://www.crefeldensis.de'
  },
  {
    name: 'Castrum Bonnense',
    logo: require('assets/images/reyche/castrum_bonnense.jpg'),
    stadt: 'Bonn',
    nummer: '(193)',
    url: 'http://www.castrum-bonnense.de'
  },
  {
    name: 'Mimegarda',
    logo: require('assets/images/reyche/mimegarda.jpg'),
    stadt: 'Münster',
    nummer: '(209)',
    url: 'http://www.mimegarda.de'
  },
  {
    name: 'Confluentia',
    logo: require('assets/images/reyche/confluentia.jpg'),
    stadt: 'Koblenz',
    nummer: '(225)',
    url: 'http://www.schlaraffia-confluentia.de'
  },
  {
    name: 'Duisbargum',
    logo: require('assets/images/reyche/duisbargum.jpg'),
    stadt: 'Duisburg',
    nummer: '(242)',
    url: 'https://www.duisbargum.de/'
  },
  {
    name: 'Gladebachum Monachorum',
    logo: require('assets/images/reyche/gladebachum.jpg'),
    stadt: 'Mönchengladbach',
    nummer: '(252)',
    url: 'http://www.gladmo252.de'
  },
  {
    name: 'Moellmia',
    logo: require('assets/images/reyche/moellmia.jpg'),
    stadt: 'Mülheim an der Ruhr',
    nummer: '(253)',
    url: 'http://www.moellmia.de'
  },
  {
    name: 'An der Sieg',
    logo: require('assets/images/reyche/an_der_sieg.jpg'),
    stadt: 'Siegen',
    nummer: '(323)',
    url: 'https://andersieg.com/'
  },
  {
    name: 'Castellum Novaesium',
    logo: require('assets/images/reyche/castellum_novaesium.jpg'),
    stadt: 'Neuss',
    nummer: '(353)',
    url: 'http://www.castellum-novaesium.de'
  },
  {
    name: 'Porta Arduennae',
    logo: require('assets/images/reyche/portaarduennae.jpg'),
    stadt: 'Düren',
    nummer: '(367)',
    url: 'http://www.portaarduennae.de/'
  },
  {
    name: 'Im Vest',
    logo: require('assets/images/reyche/imvest.jpg'),
    stadt: 'Gelsenkirchen',
    nummer: '(373)',
    url: 'http://www.imvest373.de'
  },
  {
    name: 'Sugambria',
    logo: require('assets/images/reyche/sugambria.jpg'),
    stadt: 'Lohmar',
    nummer: '(398)',
    url: 'http://www.schlaraffia-sugambria.de'
  },
  {
    name: 'Brucsella',
    logo: require('assets/images/reyche/bruscella.jpg'),
    stadt: 'Brüssel',
    nummer: '(418)',
    url: 'http://www.brucsella.os-home.de'
  },
];
export default {
  data: () => ({
    reyche: alleNachbarn
  })
}
</script>
<style lang="scss" scoped>
.nachbarn {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-column-gap: 16px;
    grid-row-gap: 16px;
}
.reych {
  display: flex;
  align-items: center;
  flex-direction: column;
  text-align: center;
  margin: 0 auto;
  max-width: 300px;
  width: 300px;
  border-radius: 16px;
  transition: all ease-in-out 320ms;
  padding: 3rem;
  border: solid 1px rgb(0 0 0 / 10%);
  color: #0B7CB8;

  &:hover {
    box-shadow: rgb(0 0 0 / 10%) 0px 20px 25px -5px, rgb(0 0 0 / 4%) 0px 10px 10px -5px;
    background: #ffffff;
  }

  img {
    max-width: 100px;
    width: 100px;
  }

  &__content {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin-top: 1rem;
    font-weight: bold;
  }

  &__city {
    font-style: italic;
    color: #777;
    font-weight: 300;
    margin-top: 0.5rem;
  }
}
.main {
  min-height: calc(100vh - 400px);
}
</style>

