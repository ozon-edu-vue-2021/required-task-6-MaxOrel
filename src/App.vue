<template>
  <div id="app">
    <v-table
        :show-pagination="true"
        :show-scroll="false"
    >
    </v-table>
  </div>
</template>

<script>
import vTable from './components/Table/v-table'
export default {
  name: 'App',
  components: {
    vTable
  },
}
</script>

<style>
body {
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding-top: 60px;
}
</style>
