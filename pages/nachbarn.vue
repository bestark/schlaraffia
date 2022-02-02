<template>
  <div>
    <Layout-HeaderPart>
      Unsere Nachbarn
    </Layout-HeaderPart>
    <main class="main">
      <section class="section">
        <div class="container is-fullhd px-4">
          <Layout-LeftRightText>
            <template v-slot:title>Verweise zu Nachbar-Reychen</template>
            By creating a visual guide along the way, the designer or developer can get input from the other people
            involved in the website such as the customer, their manager, and other members of the team.By creating a
            visual guide along the way, the designer or developer can get input from the other people involved in the
            website such as the customer, their manager, and other members of the team.
          </Layout-LeftRightText>
        </div>
      </section>
      <section class="section">
        <div class="container nachbarn is-fullhd px-4">
          <a :href="reych.url" target="_blank" class="reych" v-for="reych of reyche" :key="reyche.nummer">
            <img :src="reych.logo" />
            {{reych.name}}
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
    stadt: '',
    nummer: '(8)',
    url: 'http://www.schlaraffia-colonia-agrippina.de"'
  },
  {
    name: 'Elberfeldensis',
    logo: require('assets/images/reyche/elberfeldensis.jpg'),
    stadt: '',
    nummer: '(34)',
    url: 'http://www.elberfeldensis.de"'
  },
  {
    name: 'Assindia',
    logo: require('assets/images/reyche/assindia.jpg'),
    stadt: '',
    nummer: '(50)',
    url: 'http://www.schlaraffia-assindia.org"'
  },
  {
    name: 'Aquisgranum',
    logo: require('assets/images/reyche/aquisgranum.jpg'),
    stadt: '',
    nummer: '(94)',
    url: 'http://www.aquisgranum.de"'
  },
  {
    name: 'Bochumensis',
    logo: require('assets/images/reyche/bochumensis.jpg'),
    stadt: '',
    nummer: '(166)',
    url: 'http://www.bochumensis.de"'
  },
  {
    name: 'Truymannia',
    logo: require('assets/images/reyche/truymannia.jpg'),
    stadt: '',
    nummer: '(177)',
    url: 'http://www.truymannia.de"'
  },
  {
    name: 'Hagena',
    logo: require('assets/images/reyche/hagena.jpg'),
    stadt: '',
    nummer: '(189)',
    url: 'http://www.schlaraffia-hagena.de"'
  },
  {
    name: 'Crefeldensis',
    logo: require('assets/images/reyche/crefeldensis.jpg'),
    stadt: '',
    nummer: '(191)',
    url: 'http://www.crefeldensis.de"'
  },
  {
    name: 'Castrum Bonnense',
    logo: require('assets/images/reyche/castrum_bonnense.jpg'),
    stadt: '',
    nummer: '(193)',
    url: 'http://www.castrum-bonnense.de"'
  },
  {
    name: 'Mimegarda',
    logo: require('assets/images/reyche/mimegarda.jpg'),
    stadt: '',
    nummer: '(209)',
    url: 'http://www.mimegarda.de"'
  },
  {
    name: 'Confluentia',
    logo: require('assets/images/reyche/confluentia.jpg'),
    stadt: '',
    nummer: '(225)',
    url: 'http://www.schlaraffia-confluentia.de"'
  },
  {
    name: 'Duisbargum',
    logo: require('assets/images/reyche/duisbargum.jpg'),
    stadt: '',
    nummer: '(242)',
    url: 'http://www.schlaraffia-duisbargum.de"'
  },
  {
    name: 'Gladebachum Monachorum',
    logo: require('assets/images/reyche/gladebachum.jpg'),
    stadt: '',
    nummer: '(252)',
    url: 'http://www.gladmo252.de"'
  },
  {
    name: 'Moellmia',
    logo: require('assets/images/reyche/moellmia.jpg'),
    stadt: '',
    nummer: '(253)',
    url: 'http://www.moellmia.de"'
  },
  {
    name: 'An der Sieg',
    logo: require('assets/images/reyche/an_der_sieg.jpg'),
    stadt: '',
    nummer: '(323)',
    url: 'http://www.andersieg.de"'
  },
  {
    name: 'Castellum Novaesium',
    logo: require('assets/images/reyche/castellum_novaesium.jpg'),
    stadt: '',
    nummer: '(353)',
    url: 'http://www.castellum-novaesium.de"'
  },
  {
    name: 'Porta Arduennae',
    logo: require('assets/images/reyche/portaarduennae.jpg'),
    stadt: '',
    nummer: '(367)',
    url: 'http://www.portaarduennae.de/"'
  },
  {
    name: 'Im Vest',
    logo: require('assets/images/reyche/imvest.jpg'),
    stadt: '',
    nummer: '(373)',
    url: 'http://www.imvest373.de"'
  },
  {
    name: 'Sugambria',
    logo: require('assets/images/reyche/sugambria.jpg'),
    stadt: '',
    nummer: '(398)',
    url: 'http://www.schlaraffia-sugambria.de"'
  },
  {
    name: 'Brucsella',
    logo: require('assets/images/reyche/bruscella.jpg'),
    stadt: '',
    nummer: '(418)',
    url: 'http://www.brucsella.os-home.de"'
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
  text-align: center;
  margin: 0 auto;
  max-width: 300px;
  border-radius: 16px;
  transition: all ease-in-out 320ms;
  padding: 3rem 1rem;

  &:hover {
    box-shadow: rgba(0, 0, 0, 0.1) 0px 20px 25px -5px, rgba(0, 0, 0, 0.04) 0px 10px 10px -5px;
    background: #ffffff;
  }
}
.main {
  min-height: calc(100vh - 400px);
}
</style>

