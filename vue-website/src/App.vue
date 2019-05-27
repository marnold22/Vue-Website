<template>
  <div id="app">

    <nav class="navbar">
      <div class="navbar-brand">
        <a class="navbar-item">MyCompany</a>

        <a class="navbar-burger burger" v-on:click="toggleNav" v-bind:class="{'is-active': isActive}">
          <span></span>
          <span></span>
          <span></span>
        </a>
      </div>

      <div class="navbar-menu" v-bind:class="{'is-active': isActive}">
        <div class="navbar-end">
          <router-link to="/" class="navbar-item r-item">Home</router-link>
          <router-link to="/faq" class="navbar-item r-item">About</router-link>
          <router-link to="/faq" class="navbar-item r-item">Contact</router-link>
          <router-link to="/faq" class="navbar-item r-item">FAQ</router-link>
          <div class="navbar-item">
            <a class="button is-primary is-outlined">
              <span class="icon">
                <i class="fa fa-download"></i>
              </span>
              <span>Join Now</span>
            </a>
          </div>
        </div>
      </div>
    </nav>

    <router-view></router-view>

    <footer class="footer is-primary">
      <div class="container">
        <div class="columns">
          <div class="column">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p>
          </div>
          <div class="column has-text-right">
            <a class="icon" href="#"><i class="fab fa-facebook-square fa-2x"></i></a>
            <a class="icon" href="#"><i class="fab fa-twitter-square fa-2x"></i></a>
          </div>
        </div>
      </div>
    </footer>

  </div>
</template>

<script>
export default {
  name: 'App',
  data: function() {
    return {
      isActive: false
    }
  },
  methods: {
    toggleNav: function() {
      this.isActive = !this.isActive;
    }
  }
}
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'mq'

.navbar
  background-color: #383838
  a:hover
    color: gray

.r-item
  color: #C1C1C1
  padding: 0.5rem 1.75rem
  &:hover
    background-color: #383838
  +mobile
    color: gray
    &:hover
      background-color: #f1f1f1


.navbar-brand .navbar-item
  color: #C1C1C1
  font-weight: bold

.navbar-burger span
  background-color: #c1c1c1

footer
  background-color: $primary !important
  color: #fff

  .icon
    color: #fff
    margin-left: 20px

</style>
