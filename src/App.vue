<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
html{
  height: 100%;
  font-size: 10vw;
  padding: 0;
  margin: 0;
}
body {
  font-size: 16px;
  width: 100%;
  height: 100%;
  margin: 0 auto;
}

@media screen and (min-width: 750px) {
  html{
    font-size: 40Px;
  }
  body{
    max-width: 750Px;
  }
}


#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
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
