<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Take your chances</router-link> |
      <router-link to="/props">sry </router-link>
      <router-link to="/form">| shh</router-link>
    </div>
    <router-view />
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
