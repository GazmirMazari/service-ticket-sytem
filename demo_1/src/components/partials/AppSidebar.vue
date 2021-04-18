<template lang="html">
  <section class="app-sidebar">
    <nav class="sidebar sidebar-offcanvas" id="sidebar">
      <ul class="nav">
        <li class="nav-item nav-profile">
          <a href="#" class="nav-link">
            <div class="profile-image">
              <img class="img-xs rounded-circle" src="../../assets/images/faces/face8.jpg" alt="profile image">
              <div class="dot-indicator bg-success"></div>
            </div>
            <div class="text-wrapper">
              <p class="profile-name">Gazmir Mazari</p>
            </div>
          </a>
        </li>
        <li class="nav-item nav-category">Main Menu</li>
        <li class="nav-item">
          <a class="nav-link" v-b-toggle="'dashboard-dropdown'">
            <i class="menu-icon typcn typcn-document-text"></i>
            <span class="menu-title">Dashboards</span>
            <i class="menu-arrow"></i>
          </a>
          <b-collapse id="dashboard-dropdown">
            <ul class="nav flex-column sub-menu">
              <li class="nav-item">
                <router-link class="nav-link" to="/">Interactive Dashboard</router-link>
              </li>
            </ul>
          </b-collapse>
        </li>
      </ul>
    </nav>
  </section>
</template>

<script lang="js">
import JQuery from 'jquery'
// eslint-disable-next-line
let $ = JQuery
export default {
  name: 'app-sidebar',
  mounted () {
    const body = document.querySelector('body')
    // add class 'hover-open' to sidebar navitem while hover in sidebar-icon-only menu
    document.querySelectorAll('.sidebar .nav-item').forEach(function (el) {
      el.addEventListener('mouseover', function () {
        if (body.classList.contains('sidebar-icon-only')) {
          el.classList.add('hover-open')
        }
      })
      el.addEventListener('mouseout', function () {
        if (body.classList.contains('sidebar-icon-only')) {
          el.classList.remove('hover-open')
        }
      })
    })
  }
}
</script>

<style scoped lang="scss">
.app-sidebar {
}
</style>
