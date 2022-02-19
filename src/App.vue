<template>
  <div id="nav">
    {{name}}
    <ul>
      <li>1
        <p></p>
      </li>
      <li>2
        <p></p>
      </li>
      <li>3
        <p></p>
      </li>
    </ul>
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
