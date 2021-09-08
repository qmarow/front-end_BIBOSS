<template>
  <div class="header">
    <Header />
  </div>
  <div class="menuBar">
    <MenuBar />
  </div>
  <div class="contentPage">
    <ContentPage/>
  </div>
</template>


<script>
import Header from './components/Header.vue'
import MenuBar from './components/MenuBar.vue'
import ContentPage from './components/ContentPage.vue'
export default {
  props: {},
  data() {
    return {}
},
  components: {
    Header: Header,
    MenuBar: MenuBar,
    ContentPage: ContentPage,
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
  background-color: rgb(255, 255, 255);
}

.contentPage {
  position: relative;
  display: block;
  background-color: rgb(215, 248, 215);
  width: 78%;
  height: 100%;
  left: 265px;
  top: 48px
}

</style>