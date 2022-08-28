<template>
  <div class="download-box">
    <div class="content">
      <img class="download-img" src="/images/direkter-download.png">
      <h2><slot name="title"></slot></h2>
      <h4><slot name="subtitle"></slot></h4>
      <a class="button" :href="dokument">{{ docTitle }}</a>
    </div>
  </div>
</template>
<script>
export default {
  props: ['dokument', 'docTitle']
}
</script>
<style lang="scss" scoped>
.download-box {
  position: relative;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  column-gap: 1rem;
}
.content {
  position: relative;
}
.download-img {
  opacity: 0.1;
  position: absolute;
  left: 1rem;
  top: 85%;
  transform: translateY(-50%);
  width: 55px;
}
.content {
  flex: 1 1;
  background-color: lighten($color-main-blue, 50%);
  max-width: 600px;
  border-radius: 1rem;
  padding: 2rem;
  margin: 0 auto;
  text-align: center;
  box-shadow: rgb(0 0 0 / 10%) 0px 20px 25px -5px, rgb(0 0 0 / 4%) 0px 10px 10px -5px;
  transition: all ease-in-out 300ms;

  &:hover {
    transform: rotate(1deg);
  }

  .button {
    margin-top: 2rem;
  }
}
</style>
