<script>
import axios from 'axios'
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import { store } from './store.js'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain
  },

  data() {
    return {
      store,
    }
  },
  methods: {
    callApi(url) {
      axios.get(url)
        .then(response => {
          console.log(response);
          store.characters = response.data
        })
        .catch(err => {
          console.error(err.message);
          store.error = err.message
        })
    }
  },
  mounted() {
    this.callApi(store.API_URL)
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
</template>

<style lang="scss" scoped>

</style>
