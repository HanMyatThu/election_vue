<template>
  <header class="site-header">
    <nav class="navbar shadow-sm fixed-top navbar-light bg-white">
      <a class="navbar-brand">
        <img src="https://elect.in.th/wp-content/uploads/2018/10/site-logo.png">
        <h6>In Vote We Trust</h6>
      </a>
      <div class="ml-auto d-flex navbar-more">
        <router-link to="/"><h2>Home</h2></router-link>
        <router-link to="/information"><a href=""><h2>Information</h2></a></router-link>
        <router-link to="/election"><h2>Election</h2></router-link>
        <router-link to="/map"><h2>Map</h2></router-link>
      </div>
      
  </nav>


  </header>
</template>

<script>
export default {
  name: "Header"
}
</script>



