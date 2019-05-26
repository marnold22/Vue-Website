<template>
  <div id="app">

    <nav class="navbar has-shadow">
      <div class="container">

        <div class="navbar-brand">
          <a class="navbar-item">MyCompany</a>
        </div>

        <span class="navbar-toggle">
          <span></span>
          <span></span>
          <span></span>
        </span>

        <div class="navbar-end navbar-menu">
          <router-link to="/" class="navbar-item r-item">Home</router-link>
          <router-link to="/faq" class="navbar-item r-item">About</router-link>
          <router-link to="/faq" class="navbar-item r-item">Contact</router-link>
          <router-link to="/faq" class="navbar-item r-item">FAQ</router-link>

          <div class="navbar-item">
            <p class="control">
              <a class="button is-primary is-outlined">
                <span class="icon">
                  <i class="fa fa-download"></i>
                </span>
                <span>Join Now</span>
              </a>
            </p>
          </div>
        </div>
      </div>
    </nav>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'mq'

</style>
