<template>
  <b-container fluid id="app">
    <b-row>
      <b-col>
        <b-img src="./assets/logo.png"></b-img>
      </b-col>
    </b-row>
    <b-nav justified >
      <b-nav-item to='/' active>Home</b-nav-item>
      <b-nav-item to='/about'>About</b-nav-item>
      <b-nav-item to='/people'>People</b-nav-item>
    </b-nav>
    <router-view/>
  </b-container>
</template>

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
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
