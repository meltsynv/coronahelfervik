<template>
  <q-header class="nav">
    <q-toolbar>
      <q-toolbar-title>
        <router-link class="logo-link" to="/" exact>
          <img src="../assets/CoronaHelferLogo.svg">
        </router-link>
      </q-toolbar-title>
      <q-tabs shrink stretch align="right">
        <q-route-tab to="/helfen" label="Helfen"/>
        <q-route-tab to="/hilfe erhalten" label="Hilfe erhalten"/>
        <q-route-tab to="/informationen" label="Infos"/>
        <q-route-tab to="/jobs" label="Jobs"/>
      </q-tabs>
    </q-toolbar>
  </q-header>
</template>

<style lang="scss">
.nav{
    background-color: $secondary;
    .logo-link{
      img{
        width: auto;
        height: 55px;
        padding: 10px;
      }
    }
}
</style>