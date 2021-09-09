<template>
  <div class="redCircle">
      <FranchiseVideo />
  </div>
</template>


<script>
import FranchiseVideo from './FranchiseVideo.vue'
export default {
  props: {},
  data() {
    return {}
},
  components: {
      FranchiseVideo: FranchiseVideo,
  }
}
</script>


<style scoped>
.redCircle {
  z-index: 1;
	display: block;
	position: absolute;
	width: 100%;
	height: 800px;
	border-radius: 8px;
	/* background-color: rgba(77, 255, 32, 0.301); */
	background: linear-gradient(0deg, #ECEEF2 0%, rgba(236, 238, 242, 0) 100%);

	top: 8px;
}

</style>