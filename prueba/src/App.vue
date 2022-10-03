<template>
  <nav>
    <router-link to="/">Casita</router-link> /
    <router-link to="/about">Mas</router-link> /
    <router-link to="/Clientes">Clientes</router-link> /
    <router-link to="/Productos">Producto</router-link>
  </nav>
  <div class="container mt-3">
    <router-view/>
  </div>
</template>