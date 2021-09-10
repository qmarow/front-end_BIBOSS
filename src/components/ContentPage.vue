<template>
  <div class="redCircle">
      <FranchiseVideo />
  </div>
  <div id='personalSolutionW'>
    <PersonalSolutionW />
  </div>
  <div :style="{'display': 'flex'}">
    <div id="aboutCompany">
      <AboutCompany />
    </div>
    <div id="Indicators">
      <Indicators />
    </div>
  </div>
</template>


<script>
import FranchiseVideo from './partsContentPage/FranchiseVideo.vue'
import PersonalSolutionWindow from './partsContentPage/PersonalSolutionWindow.vue'
import AboutCompany from './partsContentPage/AboutCompany.vue'
import Indicators from './partsContentPage/Indicators.vue'
export default {
  props: {},
  data() {
    return {}
},
  components: {
      FranchiseVideo: FranchiseVideo,
      PersonalSolutionW: PersonalSolutionWindow,
      AboutCompany: AboutCompany,
      Indicators: Indicators,
  }
}
</script>


<style scoped>
.redCircle {
  z-index: 1;
	display: block;
	position: relative;
	width: 100%;
	height: 800px;
	border-radius: 8px;
	/* background-color: rgba(77, 255, 32, 0.301); */
	background: linear-gradient(0deg, #ECEEF2 0%, rgba(236, 238, 242, 0) 100%);

	top: 8px;
}

#personalSolutionW {
  left: calc(50% - 560px);
  top: 720px;
  position: absolute;
  z-index: 190;
}

#aboutCompany {
  padding-left: 10.5%;
  margin-top: 126px;
  position: relative;
  /* background-color: aqua; */
}

#Indicators {
  margin-top: 126px;
  margin-left: 32px;
}

</style>