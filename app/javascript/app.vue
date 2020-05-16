<template>
  <v-app id="app">
    <Header/>
    <h1>This is app.vue</h1>
    <p>{{ message }}</p>
  </v-app>
</template>

<script>
import Header from "./components/Header";

export default {
  data: function () {
    return {
      message: "Hello Vue!"
    }
  },
  components: {
    Header,
  }
}
</script>