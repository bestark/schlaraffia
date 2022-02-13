<template>
  <div class="section">
    <div class="section__title">
      <h2>
        <slot name="title"/>
      </h2>
    </div>
    <div class="section__text">
      <p :style="{'column-count': columns}">
        <slot/>
      </p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    columns: {
      type: String,
      default: '2',
      required: false
    }
  }
}
</script>
<style lang="scss" scoped>
.section {
  display: flex;
  flex-direction: column;

  &__title {
    margin-bottom: 1rem;
  }

  &__text {
  }
}
</style>
