<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/products">Products</router-link> |
    <router-link to="/admin">Admin</router-link>
  </nav>
  <router-view />
</template>

<script>
let arrayData = [
  {
    operatingSystem: "Windows 10",
    price: 1200,
    image: "https://i.postimg.cc/zByxfDBX/Windows.jpg"
  },
  {
    operatingSystem: "Ubuntu Linux",
    price: 980,
    image: "https://i.postimg.cc/QMx6RJZ7/Linux.jpg"
  },
  {
    operatingSystem: "Mac",
    price: 2000,
    image: "https://i.postimg.cc/25cHmLCK/Mac.jpg"
  }
]
localStorage.setItem('data', JSON.stringify(arrayData));
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
