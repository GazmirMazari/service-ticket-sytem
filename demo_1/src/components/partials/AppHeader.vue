<template lang="html">
  <b-navbar id="template-header" class="navbar default-layout col-lg-12 col-12 p-0 fixed-top d-flex flex-row" toggleable="md">
    <div class="text-center navbar-brand-wrapper d-flex align-items-top justify-content-center">
      <router-link class="navbar-brand brand-logo" to="/">
        <img src="../../assets/images/logo_dark.svg" alt="logo" />
      </router-link>
      <router-link class="navbar-brand brand-logo-mini" to="/">
        <img src="../../assets/images/logo_dark_mini.svg" alt="logo" />
      </router-link>
    </div>
    <div class="navbar-menu-wrapper d-flex align-items-center ml-auto ml-lg-0">
      <button class="navbar-toggler navbar-toggler align-self-center" type="button" @click="collapedSidebar()">
        <span class="mdi mdi-menu"></span>
      </button>
      <b-navbar-nav class="navbar-nav-right ml-auto">
        <form class="mr-auto search-form d-none d-md-block">
          <div class="itRoiTitle" >
              Service Desk Metrics
          </div>
        </form>
        <b-nav-item-dropdown right class="preview-list user-dropdown d-md-block">
          <template slot="button-content">
            <div class="d-flex align-items-right">
              <img class="img-xs rounded-circle" src="../../assets/images/faces/face8.jpg" alt="Profile image">
            </div>
          </template>
          <b-dropdown-item>
            <div class="dropdown-header text-center w-100">
              <img class="img-md rounded-circle" src="../../assets/images/faces/face8.jpg" alt="Profile image">
              <p class="mb-1 mt-3 font-weight-semibold">Gazmir Mazari</p>
              <p class="font-weight-light text-muted mb-0">@gmail.com</p>
            </div>
          </b-dropdown-item>
          <b-dropdown-item>My Profile <span class="badge badge-pill badge-danger">1</span><i class="dropdown-item-icon ti-dashboard"></i></b-dropdown-item>
          <b-dropdown-item>Messages<i class="dropdown-item-icon ti-comment-alt"></i></b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
      <button class="navbar-toggler navbar-toggler-right align-self-center" type="button" @click="collapedMobileSidebar()">
        <span class="mdi mdi-menu"></span>
      </button>
    </div>
  </b-navbar>
</template>

<script lang="js">
// eslint-disable-next-line
import JQuery from 'jquery'
let $ = JQuery
export default {
  name: 'app-header',
  methods: {
    collapedSidebar: function () {
      $('body').toggleClass('sidebar-icon-only')
    },
    collapedMobileSidebar: function () {
      $('#sidebar').toggleClass('active')
    }
  }
}
</script>

<style scoped lang="scss">
.app-header {
}
</style>
