<template>
  <div class="FranchiseVideo">
      <FranchiseVideo />
  </div>
  <div id='personalSolutionW'>
    <PersonalSolutionW />
  </div>
  <div :style="{'display': 'flex', 'width': '100%', 'justify-content': 'center'}">
    <div id="aboutCompany">
      <AboutCompany />
    </div>
    <div id="Indicators">
      <Indicators />
    </div>
  </div>
  <div id="OtherParticipants">
    <hr />
    <OtherParticipants />
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
}

#personalSolutionW {
  width: 100%;
  display: flex;
  justify-content: center;
  top: 720px;
  position: absolute;
  z-index: 190;
}

#aboutCompany {
  margin-top: 126px;
  position: relative;
}

#Indicators {
  margin-top: 126px;
  margin-left: 32px;
  height: 300px;
  position: sticky;
  top: 60px;
}

#OtherParticipants {
  margin-top: 24px;
  display: flex;
  align-items: center;
  flex-direction: column;
}

hr {
  margin: 0px;
  width: 1120px;
  border: 0px;
  height: 1px;
  background-color: rgba(0, 0, 0, 0.2);;
}

@media (max-width: 1130px) {
  #personalSolutionW {
    margin-top: 32px;
    position: static;
  }
  .FranchiseVideo {
    height: fit-content;
  }
  #Indicators {
    display: none;
  }
  #aboutCompany {
    margin-top: 32px;
    width: 96%;
  }
  hr {
    width: 96%;
  }
}

@media (max-width: 830px) {
  hr {
    display: none;
  }
}

</style>