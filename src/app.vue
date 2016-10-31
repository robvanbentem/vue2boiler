<template>
  <div class="main">
    <h3>Ahooi kapitein!</h3>
    <img src="./assets/logo.png">

    <div class="container">
      <ol class="breadcrumb">
        <li class="breadcrumb-item">
          <router-link to="/">Home</router-link>
        </li>
        <li class="breadcrumb-item">
          <router-link to="/simple">Simple page</router-link>
        </li>
      </ol>
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  watch: {
    '$route': (to, from) => {
      console.log('route changed to', to.path)
    }
  }
}
</script>

<style scoped lang="sass">
  .main
    font-family: 'Avenir', Helvetica, Arial, sans-serif
    -webkit-font-smoothing: antialiased
    -moz-osx-font-smoothing: grayscale
    text-align: center
    color: #2c3e50
    margin-top: 60px

    div.container
      margin-top: 30px
      text-align: left
</style>
