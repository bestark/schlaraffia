<template>
  <section class="hero">
    <div class=" container is-fullhd is-flex is-align-items-center px-4">
      <div class="columns">
        <div class="column is-three-fifths is-flex is-align-items-center">
          <div>
            <h3>Schlaraffia® Dusseldorpia e.V.</h3>
            <h1>
              Willkommen bei Schlaraffia Dusseldorpia
            </h1>
            <h2>Ein Verein wie sonst keiner</h2>
          </div>
        </div>
        <div>
          <img src="~/assets/images/hero-schlaraffe.png" alt="" class="hero-schlaraffe">
        </div>
      </div>
    </div>
  </section>
</template>
<script>

</script>
<style lang="scss" scoped>
.hero {
  color: #fff;
  background-color: #0B7CB8;
  min-height: 60vh;
  position: relative;
  overflow: hidden;
  align-items: center;
  background-image: url("~/assets/images/red-bg.svg");
  background-position: center right;
  background-size: 100vh;
  background-repeat: no-repeat;
}

.hero-schlaraffe {
  z-index: 12;
  position: relative;
}

.hero-wave {
  position: absolute;
  right: 0;
  top: 0;;
  z-index: 1;
}
</style>
