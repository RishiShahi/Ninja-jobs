<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link :to="{name: 'about'}">About</router-link> | 
    <router-link :to="{name: 'jobs'}">Jobs</router-link>
  </nav>

  <button @click="redirect">Redirect</button>
  <button @click="back"> Go Back</button>
  <button @click="forward">Go Forward</button>

  <router-view/>
</template>

<script>
   export default {
    methods: {
      redirect(){
        this.$router.push({ name: 'home'})
      },
      back() {
        this.$router.go(-1)
      },
      forward() {
        this.$router.go(1)
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
  text-decoration: none;
}

nav a.router-link-exact-active {
  color: white;
  background: crimson;
  padding: 10px;
   border-radius: 5px;
}

button{
  margin: 0 10px;
  padding: 8px 10px;
  border-radius: 5px;
  background: rgb(150, 145, 145);
  color: white;
  outline: none;
  cursor: pointer;
  border: none;
}
</style>
