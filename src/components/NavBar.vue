<template>
  <b-navbar toggleable="md" type="dark" variant="dark" id='nav'>
    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

    <b-navbar-brand>
      <router-link to="/">Home</router-link>
    </b-navbar-brand>

    <b-collapse is-nav id="nav_collapse">
      <b-navbar-nav>
        <b-nav-item>
          <router-link to="/about">About</router-link>
        </b-nav-item>

        <b-nav-item>
          <router-link to="/test">Test</router-link>
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
    name:'NavBar'
}
</script>

<style>
#nav a {
  font-weight: bold;
  color: #23c3df;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
