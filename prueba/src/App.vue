<template>
  <nav>
    <router-link to="/">Casita</router-link> /
    <router-link to="/about">Mas</router-link> /
    <router-link to="/Cliente">Cliente</router-link>
  </nav>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #474747;
}

nav a.router-link-exact-active {
  color: #f9f9fa;
}



</style>
