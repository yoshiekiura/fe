<template>
  <router-view />
</template>

<script>
import { mapActions } from 'vuex'

export default {
  async created() {
    this.getPriceTrx()
    setInterval(this.getPriceTrx, 6e4)
  },
  methods: {
    ...mapActions(['getPriceTrx']),
  },
}
</script>

<style lang="scss">
// Import Main styles for this application
@import 'styles/style';

#app {
  font-family: 'Courier New', Courier, monospace;
}

a {
  text-decoration: none;
}

.copy {
  cursor: pointer;
}
</style>
