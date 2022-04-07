<template>
  <div>
    <Layout-HeaderPart>
      Kontakt
      <template #subline>
        So sind wir zu erreichen
      </template>
    </Layout-HeaderPart>
    <main class="main">
      <section class="section">
        <div class="container is-fullhd px-4 split">
          <div class="split__content">
            <h3>Man muss es erlebt haben, um es sich vorstellen zu können.<br></h3>
            <h4>Neugierig geworden?</h4><br><br>

            Dann wir freuen uns schon, Sie bald einmal als Gast (Pilger) bei der Schlaraffia® Dusseldorpia begrüßen zu dürfen.<br>

            Unser Wappentier - der weise Uhu – garantiert:<br>
            Einen Abend, den Sie nie vergessen werden !<br><br>

            Anschrift des Kantzlers:	Werner Engels (Rt. Effendi)<br>
            Aachener Str. 11, 40223 Düsseldorf<br>
            Tel.: +49(0)211 311 02 75<br>
            Fax: +49(0)211 311 24 53<br><br>

            E-Mail: <a href="mailto:Kantzlerambt@schlaraffia-dusseldorpia.de">Kantzlerambt@schlaraffia-dusseldorpia.de</a><br><br><br>


            <b>Reychsuhunetzmeister</b>:	DI Eckart E. Glüer (Rt. Terabeyt)<br>
            (Webmaster)<br>
            Tel.: +49(0)211 979 03-12<br>
            Fax: +49(0)211 979 03-20<br>

            E-Mail: <a href="mailto:webmaster@schlaraffia-dusseldorpia.de">webmaster@schlaraffia-dusseldorpia.de</a><br>
          </div>
          <div class="split__content">
            <div>
              <h3>Anfahrt zur Burg</h3>

              Jan Wellem Burg<br>
              Parkstraße 62<br>
              40477 Düsseldorf<br><br>
            </div>
            <iframe
              class="map"
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2497.961361564591!2d6.782515015760101!3d51.23820647959179!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47b8c98bbed8baf5%3A0x203945480a933537!2sParkstra%C3%9Fe%2062%2C%2040477%20D%C3%BCsseldorf!5e0!3m2!1sde!2sde!4v1644786450184!5m2!1sde!2sde"
              height="450"
              style="border:0;"
              allowfullscreen=""
              loading="lazy"></iframe>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>
<script>
export default {
  async asyncData({$content, params, error}) {
    let post;
    try {
      post = await $content("pages", 'kontakt').fetch();
    } catch (e) {
      error({message: "Content not found"});
    }

    return {
      post,
    };
  },
};
</script>
<style lang="scss" scoped>
.map {
  width: 100%;
}
.split {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  &__content {
    width: 50%;
    &:last-child {
      border-top: 1px solid $color-main-blue;
      margin-top: 2rem;
      padding-top: 2rem;
    }
  }
}
</style>
