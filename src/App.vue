<template>
  <div id="app">
    <nav class="navbar navbar-dark bg-dark">
      <div id="nav">
        <router-link to="/User">
          <b-icon
            icon="basket2-fill"
            style="width: 30px; height: 30px"
          ></b-icon>
        </router-link>
        |
        <router-link to="/">Product</router-link>
      </div>
      <div>
        <router-link to="/User">
          <button
            type="button "
            class="btn btn-outline-success mr-1"
            @click="Submit()"
          >
            ยืนยัน
          </button>
          <button type="button" class="btn btn-outline-danger" @click="Clear()">
            Clear
          </button>
        </router-link>
      </div>
    </nav>
    <router-view />
  </div>
</template>
<script>
import { mapMutations} from "vuex";
export default {
  computed: {
    ...mapMutations(["Clear", "Submit"]),
  },
};
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
  padding: 10px;
}

#nav a {
  font-weight: bold;
  color: #ffffff;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>