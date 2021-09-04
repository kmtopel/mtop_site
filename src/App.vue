<template>
  <b-container fluid id="app">
    <b-row>
      <b-col>
        <b-img fluid src="./assets/logo.png"></b-img>
      </b-col>
    </b-row>
    <b-nav justified >
      <NavBtn url='/' text='Home' />
      <NavBtn url='/about' text='About' />
      <NavBtn url='/people' text='People' />
    </b-nav>
    <router-view/>
    <b-navbar variant="light" class='mt-3'>
      <b-container>
        <b-row>
          <b-col>
            <p>Copyright 2021</p>
          </b-col>
        </b-row>
      </b-container>
    </b-navbar>
  </b-container>
</template>

<script>
import NavBtn from '@/components/NavBtn'

export default {
  name: "app",
  components: {
    NavBtn,
  }
}
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
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
