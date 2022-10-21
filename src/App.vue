<template>
  <div id="app">
    <div class="fh5co-loader" :v-if="loader"></div>
    <nav>
      <router-link to="/">About Me</router-link> |
      <router-link to="/about">My Resume</router-link> |
      <router-link to="/skill">Skills</router-link>
    </nav>
    <router-view />
  </div>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class App extends Vue {
  loader = true;
  insertscript() {
    const scripturllist: string[] = [
      "js/jquery.min.js",
      "js/jquery.easing.1.3.js",
      "js/bootstrap.min.js",
      "js/jquery.waypoints.min.js",
      "js/jquery.stellar.min.js",
      "js/jquery.easypiechart.min.js",
      "js/main.js",
    ];
    for (let i = 0; i < scripturllist.length; i++) {
        document.getElementById("script"+i)?.remove();
    }
    const app = document.getElementById("script");
    for (let i = 0; i < scripturllist.length; i++) {
      let scriptag = document.createElement("script");
      scriptag.src = scripturllist[i];
      scriptag.id = "script" + i;
      app?.insertAdjacentElement("beforeend", scriptag);
    }
  }
  created(){
    this.insertscript();
    setTimeout(()=>{
      this.loader = false;
    },4000);
  }
  mounted(){
    if(this.loader){
      this.insertscript(); 
      this.loader = false;
    }
  }
  beforUpdate(){
    this.loader = true;
    setTimeout(()=>{
      this.loader = false;
    },4000);
  }
  updated() {
    this.insertscript();
    this.loader = false;
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

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #ff9000;
    }
  }
}
</style>
