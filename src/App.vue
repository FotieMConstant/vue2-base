<template>
  <div id="app">
    <div id="nav">
      <LocalLang />
      <router-link :to="`/${$i18n.locale}`">Home</router-link> |
      <router-link :to="`/${$i18n.locale}/about`">About</router-link>
    </div>
    <router-view />
  </div>
</template>
<script>
import LocalLang from "@/components/LocalLang.vue";
export default {
  components: {
    LocalLang,
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
