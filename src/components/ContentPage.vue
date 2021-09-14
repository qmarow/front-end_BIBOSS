<template>
  <div class="FranchiseVideo">
      <FranchiseVideo />
  </div>
  <div id='personalSolutionW'>
    <PersonalSolutionW />
  </div>
  <div :style="{'display': 'flex'}">
    <div id="aboutCompany">
      <AboutCompany />
      <hr>
      <!-- <OtherParticipants /> -->
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
import OtherParticipants from './partsContentPage/OtherParticipants.vue'
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
      OtherParticipants: OtherParticipants,
  }
}
</script>


<style scoped>
.FranchiseVideo {
  z-index: 1;
	display: flex;
  justify-content: center;
	width: 100%;
	height: 800px;
	border-radius: 8px;
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
  height: 300px;
  position: sticky;
  top: 60px;
}

hr {
  border: 0px;
  height: 1px;
  background-color: rgba(0, 0, 0, 0.2);;
}

</style>