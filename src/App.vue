<template>
  <div id="app">
    <div id="nav">
      <router-link :to="{ name: 'EventList' }">Events</router-link> |
      <router-link :to="{ name: 'About' }">About</router-link> |
      <router-link :to="{ name: 'EventCreate' }">Create Event</router-link>
    </div>
    <router-view :key="$route.fullPath" />
    <!-- The key ensures the components get loaded when the URL changes-->
    <NotificationContainer />
  </div>
</template>

<script>
import NotificationContainer from './components/NotificationContainer.vue'

export default {
  components: {
    NotificationContainer
  }
}
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

h4 {
  font-size: 20px;
}
</style>
