<template>
  <main class="hero">
    <div class="container is-fullhd is-flex is-align-items-center px-4">
      <div class="columns">
        <div class="column is-three-fifths is-flex is-align-items-center">
          <div>
            <h3>Schlaraffia® DUSSELDROPIA e.V.</h3>
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
};
</script>
<style lang="scss" scoped>
.hero {
  color: #fff;
  background-color: #0B7CB8;
  min-height: 80vh;
  position: relative;
  overflow: hidden;
  align-items: center;
  background-image: url("~/assets/images/red-bg.svg");
  background-position: right;
  background-size: 100vh;
  background-repeat: no-repeat;

  h1, h2, h3 {
    font-family: "Noto";
    font-size: 26px;
  }

  h1 {
    font-size: 60px;
  }
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

.el-main {
  padding: 0;
  max-width: 1440px;
  margin: 0 auto;
}


.el-row {
  display: flex;
  align-items: center;
}
</style>
