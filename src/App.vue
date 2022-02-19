<template>
  <div id="nav">
    {{name}}
    <p class="text-center align-items-center">測試增基文字</p>
    <p class="text-center d-flex align-items-center justify-content-center">123123</p>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
  <router-view/>
</template>

<script>
import {ref} from 'vue'
export default {
  setup() {
    const name = ref('123')
    const arry = [1,2,3,4,5,6];
    _.forEach(arry , (item) => {
      console.log(item)
    })
    return {
      name
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
