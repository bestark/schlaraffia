<template>
  <section class="intro section">
    <div class=" container is-fullhd px-4">
      <div class="intro__text has-text-centered">
        <img v-if="enableDots" src="~/assets/images/dots.svg" alt="" class="intro-dots">
        <slot/>
      </div>
      <div class="side-images">
        <img :src="imageLeft" alt="" class="left">
        <img :src="imageRight" alt="" class="right">
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    enableDots: {
      type: Boolean,
      default: true
    },
    imageRight: String,
    imageLeft: String,
  }
}
</script>
<style lang="scss" scoped>
.intro {
  padding: 8rem 0;
  background: #F6FCFF;

  .side-images {
    @include media("<=tablet") {
      text-align: center;
    }

    .left, .right {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);

      @include media("<desktop") {
        display: none;
      }
    }

    .left {
      left: 0;
    }

    .right {
      right: 0;
    }
  }

  &__text {
    max-width: 767px;
    margin: 0 auto;
    position: relative;

    p {
      margin-top: 1rem;
    }
  }

  &-dots {
    display: block;
    position: absolute;
    right: -150px;
    top: -50px;
    opacity: 0.3;
    @include media("<desktop") {
      display: none;
    }
  }

  &__benefits {
    max-width: 1024px;
    margin: 3rem auto 0;
  }
}
</style>
