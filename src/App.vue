<template>
  <div class="header">
    <Header />
  </div>
</template>


<script>
import Header from './components/Header.vue'
export default {
  props: {},
  data() {
    return {}
},
  components: {
    Header: Header,
  }
}
</script>


<style scoped>

.header {
  width: 100%;
}
</style>