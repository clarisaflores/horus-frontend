<template>
  <div class="wrapper" :class="{'nav-open': $sidebar.showSidebar}">
    <notifications></notifications>

    <side-bar>
      <mobile-menu slot="content"></mobile-menu>
      <sidebar-link to="/dashboard">
        <md-icon>local_play</md-icon>
        <p>Eventos</p>
      </sidebar-link>
      <sidebar-link to="/user">
        <md-icon>location_city</md-icon>
        <p>Escuelas</p>
      </sidebar-link>
      <sidebar-link to="/reports">
        <md-icon>school</md-icon>
        <p>Alumnos</p>
      </sidebar-link>
      <sidebar-link to="/typography">
        <md-icon>monetization_on</md-icon>
        <p>Pagos</p>
      </sidebar-link>
      <sidebar-link to="/icons">
        <md-icon>photo_camera</md-icon>
        <p>Fotos</p>
      </sidebar-link>
      <sidebar-link to="/maps">
        <md-icon>assignment</md-icon>
        <p>Reportes</p>
      </sidebar-link>
      <sidebar-link to="/notifications">
        <md-icon>people</md-icon>
        <p>Usuarios</p>
      </sidebar-link>
    </side-bar>

    <div class="main-panel">
      <top-navbar></top-navbar>

      <dashboard-content>

      </dashboard-content>

      <content-footer v-if="!$route.meta.hideFooter"></content-footer>
    </div>
  </div>
</template>
<style lang="scss">

</style>
<script>
import TopNavbar from './TopNavbar.vue'
import ContentFooter from './ContentFooter.vue'
import DashboardContent from './Content.vue'
import MobileMenu from '@/pages/Layout/MobileMenu.vue'

export default {
  components: {
    TopNavbar,
    DashboardContent,
    ContentFooter,
    MobileMenu
  }
}
</script>
