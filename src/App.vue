<template>
  <div class="header">
    <Header />
  </div>
  <div class="menuBar">
    <MenuBar />
  </div>
</template>


<script>
import Header from './components/Header.vue'
import MenuBar from './components/MenuBar.vue'
export default {
  props: {},
  data() {
    return {}
},
  components: {
    Header: Header,
    MenuBar: MenuBar,
  }
}
</script>


<style scoped>

.header {
  width: 100%;
  position: fixed;
  background-color: #fff;
}

.menuBar {
  /* display: block; */
  position: fixed;
  top: 56px;
  width: 304px;
  height: 100%;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-left-width: 0px;
  border-top-width: 0px;
  border-bottom-width: 0px;

  z-index: 199;
  /* background-color: rgb(255, 255, 255); */
}
</style>