<template>
  <footer class="footer">
    <div class="footer__inner container is-fullhd">
      <div class="columns">
        <div class="column">© {{ year }} Schlaraffia® Dusseldorpia e.V.</div>
        <div class="column is-flex is-justify-content-flex-end">
          <ul class="footer__list">
            <li>
              <NuxtLink to="impressum">Impressum</NuxtLink>
            </li>
            <li>
              <NuxtLink to="datenschutz">Datenschutz</NuxtLink>
            </li>
            <li>
              <a href="https://www.allschlaraffia.de">Allschlarafia </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  computed: {
    year() {
      const now = new Date();
      return now.getFullYear();
    }
  }
}

</script>
<style lang="scss" scoped>
.footer {
  padding: 0;
  background-color: $color-main-blue;
  color: #ffffff;
  margin-bottom: 6px;
  position: relative;

  &:after {
    position: absolute;
    bottom: -6px;
    content: ' ';
    display: block;
    width: 100%;
    height: 6px;
    background-color: $color-main-red;
  }

  &__inner {
    padding: 0 1rem;
  }

  &__list {
    list-style: none;

    li {
      display: inline-block;
      margin-left: 1rem;

      a {
        color: #ffffff;
      }

      &:hover {
        text-decoration: none;
      }
    }
  }

  .column {
    @media (max-width: 768px) {
      text-align: center;
      justify-content: center !important;
    }
  }
}
</style>
