<template>
  <div class="teaser">
    <div class="teaser__content">
      <img class="teaser__image" src="" alt="" />
      <h5 class="teaser__overline"><span>{{ post.category }}</span><span class="teaser__date">{{postDate}}</span></h5>
      <h3 class="teaser__title">{{ post.title }}</h3>
      <p class="teaser__text">{{post.description}}</p>
    </div>
    <NuxtLink class="teaser__link" :to="`blog/${post.slug}`">Mehr lesen ></NuxtLink>
  </div>
</template>
<script>
export default{
  props: ["post"],
  computed: {
    postDate() {
      return new Date(this.post.date).getMonth() + 1 + '.' + new Date(this.post.date).getFullYear();
    }
  }
}
</script>
<style lang="scss" scoped>
.teaser {
  border-radius: 8px;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 20px 25px -5px, rgba(0, 0, 0, 0.04) 0px 10px 10px -5px;
  background: #ffffff;
  max-width: 360px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  &__content {
    padding: 2rem;
  }

  &__overline {
    display: flex;
    justify-content: space-between;
    text-transform: uppercase;
    font-size: 12px;
    font-weight: 500;
    letter-spacing: 1px;
    margin-bottom: 1rem;

    span {
      display: inline-block;
    }
  }

  &__title {
    font-size: 22px;
    margin-bottom: 1rem;
  }

  &__text {
    font-size: 15px;
    margin-bottom: 1rem;
  }

  &__link {
    font-size: 13px;
    text-transform: uppercase;
    color: #ffffff;
    background-color: #0B7CB8;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 50px;
    border-radius: 0 0 8px 8px;
    transition: all 175ms ease-in;

    &:hover {
      background-color: darken(#0B7CB8, 10%);
    }
  }
}
</style>
