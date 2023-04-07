<template>
  <div id="app">
<div class="container-fl">
  <div class="row">
    <div class="col-lg-3">
      <Navbar />
    </div>
    <div class="col-lg-9">
     <router-view/>
    </div>
  </div>
</div>
    
      
  
  

   
  </div>
</template>
<script>
import Navbar from "@/components/Navbar.vue"
export default {
  components:{
    Navbar
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
