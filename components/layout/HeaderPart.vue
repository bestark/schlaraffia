<template>
  <div>
    <div class="hero">
      <div class="hero__overline">
        <slot name="overline"/>
      </div>
      <h1 class="hero__title">
        <slot/>
      </h1>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.hero {
  min-height: 400px;
  background-color: #0B7CB8;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #ffffff;

  &__overline {
    text-transform: uppercase;
    letter-spacing: 1px;
    font-size: 15px;
    margin-bottom: -1rem;
  }

  &__title {
    font-weight: 700;
    font-size: 42px;
    letter-spacing: 1px;
  }
}
</style>

