<template>
	<div class="mainBlock">
		<div class="medalBlock">
			<img src="./../images/medal.svg" />
			<div class="textsMedal">
				<span :style="{'font-weight': 'normal'}">Конкурс БИБОСС</span>
				<span :style="{'font-weight': 'bold'}">«Лучшее видео о франшизе»</span>
			</div>
		</div>
		<div id="textPersonalSolution">Видео о франшизе «Персональное решение»</div>
		<div id="blockVideo">
			<video id="videoMedia" src="./../assets/FranchiseVideo.mp4" preload="auto" poster="./../images/firstCadr.jpg"/>
			<img @click="startVideo()" src='./../images/iconPlayVideo.svg' id="btnPlay" :class="controlsVisible == true ? 'btnPlayOff' : 'btnPlayOn'" />
			<div @click="closeVideo()" v-if="controlsVisible" class='menu-btn' :class="change ? 'menu-btn-1' : ''">
				<span></span>
			</div>
		</div>
	</div>
</template>


<script>
export default {
	props: {},
	data() {
		return {
			controlsVisible: false,
		}
	},
	methods: {
		startVideo() {
			var elem = document.getElementById('videoMedia');
			if (this.controlsVisible === false) {
				elem.play();
				this.controlsVisible = true;
			}
			elem.controls = true;
		},
		closeVideo() {
			var elem = document.getElementById('videoMedia');
			this.controlsVisible = false;
			elem.controls = false;
			elem.load();
		}
	},
	components: {}
}
</script>


<style scoped>

.mainBlock {
		/* position: absolute; */
	width: 100%;
	height: 800px;
	left: 304px;
	top: 860px;

	background: linear-gradient(0deg, #ECEEF2 0%, rgba(236, 238, 242, 0) 100%);
	/* transform: matrix(1, 0, 0, -1, 0, 0); */
	/* background-color: hotpink; */
}

.medalBlock {
	margin: 28px 0px 0px 48px;
	display: flex;
	width: 338px;
	height: 60px;
}

.textsMedal {
	line-height: 24px;

	font-size: 18px;
	font-family: Arial;
	font-style: normal;

	display: flex;
	flex-direction: column;
	margin-left: 16px;
	margin-top: 8px;
}

#textPersonalSolution {
	margin-top: 24px;
	margin-left: 4.4%;
	font-size: 48px;
	font-family: Arial;
	font-style: normal;
}

#blockVideo {
	margin-left: 50px;
	margin-top: 50px;
	position: relative;
	display: inline-block;
	background-color: aqua;
}

#videoMedia {
	width: 832px;
	height: 468px;
	border-radius: 16.9796px;
}

#btnPlay {
	top: calc(50% - 40px);
	left: calc(50% - 40px);
	position: absolute;
	transition: .5s;
}

.btnPlayOn {
	height: 80px;
	width: 80px;
}

.btnPlayOff {
	opacity: 0;
	height: 10px;
	width: 10px;
}

.menu-btn {
	/* margin-left: 7px; */
	top: 1%;
	left: 96%;
	border: 2px solid rgba(196, 196, 196, 0);
	display: block;
	width: 20px;
	height: 20px;
	/* background-color: rgb(228, 119, 119); */
	border-radius: 50%;
	position: absolute;
	transition: 0.3s;
}

.menu-btn:hover {
	border: 2px solid rgb(196, 196, 196);

}

.menu-btn span::before,
.menu-btn span::after 
{
	border-radius: 10px;
	width: 15px;
	height: 2px;
	background-color: rgb(196, 196, 196);
	position: absolute;
	top: 50%; margin-top: -1px;
	left: calc(50% - 7.5px);
}

.menu-btn span::before {
	transform: rotate(-45deg);
}
.menu-btn span::after 
{
	transform: rotate(45deg);
}

.menu-btn span::before,
.menu-btn span::after {
	content: '';
	display: block;
	transition: 0.1s;
}

.menu-btn:hover span::after {
	width: 12px;
	left: calc(50% - 6px);
}

.menu-btn:hover span::before {
	width: 12px;
	left: calc(50% - 6px);
}

</style>