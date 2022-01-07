<template>
  <header class="header">
    <b-navbar>
      <template #brand>
        <b-navbar-item tag="router-link" :to="{ path: '/' }">
          <img
            src="~/assets/images/logo.png"
            alt="Logo der Schlaraffen Dusseldorpia"
          >
        </b-navbar-item>
      </template>
      <template #start>
        <NuxtLink to="/">Schlaraffia Dusseldorpia</NuxtLink>
      </template>

      <template #end>
        <b-navbar-item>
          Startseite
        </b-navbar-item>
        <b-navbar-item href="#">
          Die Idee
        </b-navbar-item>
        <b-navbar-item href="#">
          Entstehung
        </b-navbar-item>
        <b-navbar-item href="#">
          Termine & Neuigkeiten
        </b-navbar-item>
        <b-navbar-item href="#">
          Unsere Nachbarn
        </b-navbar-item>
        <b-navbar-item href="#">
          Kontakt
        </b-navbar-item>
      </template>
    </b-navbar>
  </header>
</template>
<script>
</script>
<style lang="scss" scoped>

.header {
  &:before {
    content: ' ';
    display: block;
    width: 100%;
    height: 6px;
    background-color: $color-main-red;
  }
}
.navbar {
  background-color: $color-main-blue;
  padding: 0 1rem;
  box-shadow: rgba(0, 0, 0, 0.05) 0px 6px 24px 0px, rgba(0, 0, 0, 0.08) 0px 0px 0px 1px;
}

::v-deep .navbar-brand {
  align-items: center;
}


::v-deep .navbar-start {
  align-items: center;

  a {
    color: #fff;
    font-size: 22px;

    @media (max-width: 1023px) {
      color: #000;
    }
  }
}

.navbar__logo {
  display: block;
  height: 60px;
  margin-left: auto;
  margin-right: auto;
}

.navbar-item {
  color: #fff;

  @media (max-width: 1023px) {
    color: #000;

  }

  &:hover {
    color: $color-main-blue;
  }

  img {
    max-height: 3.75rem;
  }
}

::v-deep .navbar-burger {
  background-color: transparent;
  color: #fff;
}


</style>
