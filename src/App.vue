<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link>
      |
      <router-link to="/about">About</router-link>
    </nav>
    <router-view/>
    <Comp1 :label="label"/>
    <Comp2/>

  </div>
</template>

<script>
import Comp1 from '../src/components/Comp-1'
import Comp2 from '../src/components/Comp-2'

export default {
  components: {
    Comp1: Comp1,
    Comp2: Comp2
  },
  data () {
    return {
      label: 'my label'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
