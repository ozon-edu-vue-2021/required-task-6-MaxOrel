<template>
  <div id="app">
    <v-table
        :table-data="USERS"
        :show-pagination="true"
        :show-scroll="false"
    >
    </v-table>
  </div>
</template>

<script>
import {mapActions, mapGetters} from 'vuex'
import vTable from './components/Table/v-table'
export default {
  name: 'App',
  components: {
    vTable
  },
  data: () => {
    return {

    }
  },
  methods: {
    ...mapActions([
        'GET_USERS_FROM_API'
    ])
  },
  mounted() {
    this.GET_USERS_FROM_API()
  },
  computed: {
    ...mapGetters([
        'USERS'
    ])
  }
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
