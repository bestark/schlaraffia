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
          Neuigkeiten
        </b-navbar-item>
        <b-navbar-item href="#">
          Termine & Neuigkeiten
        </b-navbar-item>
        <b-navbar-item href="#">
          Nachbarreyche
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
.navbar {
  background-color: #0B7CB8;
  padding: 0 1rem;
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

.header--overline {
  width: 100%;
  height: 6px;
  background-color: #DB2F23;
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
    color: #0B7CB8;
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
