<template>
  <div id="app">
      <Burger 
      rotate="container" 
      />
    <div id="nav">
      <router-link class='nav-link' to="/">Home</router-link>
      <router-link class='nav-link' to="/about">About</router-link>
      <router-link class='nav-link' to="/about">Services</router-link>
      <router-link class='nav-link' to="/about">Contact</router-link>
    </div>
    <router-view/>
  </div>
</template>

  <script>
    import Burger from "@/components/Burger.vue"

  export default {
      name: "burger",
      components: {
        Burger
         },
  }
  </script>
  

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  display: grid;
  grid-template-areas: 
  "nav home";
  grid-template-columns: 300px;
}
#nav  {
    display: flex;
    justify-content: center;
    flex-direction: column;
    padding-top: 3rem;
    text-align: center;
    grid-area: nav;
    background: #a9c8e7;
    width: 100%;
    height: 100vh;
    position: relative;
    /* left: -300px; */

}



.nav-link {
  text-decoration: none;
  font-size: 1.5rem;
  line-height: 5.5rem;
  padding-bottom: 1.3rem;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

</style>
