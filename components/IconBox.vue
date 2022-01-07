<template>
  <div class="iconbox">
    <img src="~/assets/images/hero-schlaraffe.png" alt="" class="iconbox__icon">
    <h4>{{ title }}</h4>
    <p>{{ text }}</p>
  </div>
</template>
<script>
export default {
  props: ['title', 'text']
}
</script>
<style lang="scss" scoped>
.iconbox {
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

  &__icon {
    width: 75px;
    margin-bottom: 0.5rem;
  }

  h4 {
    font-weight: 600;
  }
}
</style>
