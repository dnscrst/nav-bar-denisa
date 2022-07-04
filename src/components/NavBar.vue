<template>
  <div class="nav-bar">
    <div class="logo">
      <img alt="logo" src="../assets/logo.png">

    </div>
    <div class="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/blog">Blog</router-link>
      <router-link to="/contact">Contact</router-link>
    </div>


  </div>
</template>

<script>
export default {
  name: 'NavBar',

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
img {
  width: 30px;

}

.nav-bar {
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
  padding: 12px 24px;

  :hover {
    color: red;


  }
}

a {
  text-decoration: none;
  margin-left: 15px;

  :hover {
    color: red;



  }
}
</style>
