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
	display: block;
	position: absolute;
	width: 100%;
	height: 1000px;
	border-radius: 8px;
	background-color: rgba(77, 255, 32, 0.301);

	top: 8px;
	left: 40px;
}

</style>