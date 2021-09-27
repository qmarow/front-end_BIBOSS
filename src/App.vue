<template>
  <div class="header">
    <Header :visibleBar="visibleBar" @changeBar="changeVisibleBar"/>
  </div>
  <div>
    <transition name="menuBar">
      <div v-if='visibleBar' class="menuBar">
        <MenuBar />
      </div>
    </transition>
    <transition name='closingBlock'>
      <div v-if='visibleBar' id="closingBlock" @click="changeVisibleBar"></div>
    </transition>
  </div>
  <div class="contentPage">
    <ContentPage/>
  </div>
  <div id="basement">
    <Basement/>
  </div>
</template>


<script>
import Header from './components/Header.vue'
import MenuBar from './components/MenuBar.vue'
import ContentPage from './components/ContentPage.vue'
import Basement from './components/Basement.vue'
export default {
  props: {},
  provide: ['width'],
  data() {
    return {
      visibleBar: false,
      width: document.body.clientWidth,
    }
  },
  mounted() {
  },
  updated() {
    console.log("!!!");
  },
  methods: {
    changeVisibleBar() {
      this.visibleBar = !this.visibleBar;
    },
    updateWidth() {
      this.width = document.body.clientWidth;
    }
  },
  components: {
    Header: Header,
    MenuBar: MenuBar,
    ContentPage: ContentPage,
    Basement: Basement,
  },
  watch: {
  },
  created() {
    window.addEventListener('resize', this.updateWidth);
  },
}
</script>


<style scoped>

.header {
  z-index: 200;
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

  transition: 0.5s;
}

.contentPage {
  z-index: 10;
  position: relative;
  /* display: block; */
  /* background-color: rgb(94, 255, 94); */
  width: 100%;
  height: 100%;
  /* left: calc(9%); */
  top: 48px
}

#basement {
  position: relative;
  top: 48px;
}

.menuBar-enter-active {
  transition: .2s;
  transform: translateX(-304px);
}

.menuBar-enter-to {
  transition: .2s;
  transform: translateX(0px);
  opacity: 1;
}
.menuBar-leave-active {
  transform: translateX(-304px);
  transition: .3s;
  opacity: 0;
}

#closingBlock {
  z-index: 190;
  position: fixed;
  top: 56px;
  background-color: rgba(34, 34, 34, 0.651);
  width: 100%;
  height: calc(100% - 56px);
}

.closingBlock-enter-active {
  transition: 0s;
  opacity: 0.5;
}.closingBlock-enter-to {
  transition: 0.2s;
  opacity: 1;
}.closingBlock-leave-active {
  transition: 0.1s;
  opacity: 0;
}

@media (max-width: 1130px) {
  #basement {
    display: none;
  }
}

</style>