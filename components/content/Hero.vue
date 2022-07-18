<template>
  <section class="hero">
    <div class=" container is-fullhd is-flex is-align-items-center px-4">
      <div class="columns">
        <div class="column is-three-fifths is-flex is-align-items-center">
          <div>
            <slot />
          </div>
        </div>
        <div>
          <img :src="image" alt="" class="hero__image">
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    image: String,
  }
}
</script>

<style lang="scss" scoped>
.hero {
  color: #fff;
  background-color: #0B7CB8;
  min-height: 60vh;
  position: relative;
  overflow: hidden;
  align-items: center;
  background-image: url("assets/images/red-bg.svg");
  background-position: center right;
  background-size: 100vh;
  background-repeat: no-repeat;

  @media (max-width: 768px) {
    background-position: center bottom;
  }
}

.hero__image {
  max-width: 90%;
  padding: 2rem;
  position: relative;
}

</style>
