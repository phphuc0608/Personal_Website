<template>
    <nav class="navbar-dark sticky-top navbar navbar-expand-lg">
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarText" aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarText" >
        <div class="navbar-nav m-auto">
          <router-link class="text-center nav-link" to="/">Home</router-link> 
          <router-link class="text-center nav-link" to="/about">About</router-link>
          <router-link class="text-center nav-link" to="/exp">Experiences</router-link>
          <router-link class="text-center nav-link" to="/project">Projects</router-link>
          <router-link class="text-center nav-link" to="/contact">Contact</router-link>
        </div>
      </div>
    </nav>
</template>

<style>
nav {
  background-color: black;
}
nav a {
  font-weight: bold;
  color: gray;
  padding-right: 15px;
  text-decoration: none;
}

nav a:hover {
  color: hsla(0,0%,100%,.75);
}

nav a.router-link-exact-active {
  color: white;
}
</style>