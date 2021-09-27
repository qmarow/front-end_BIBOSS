<template>
	<div id="bMain">
		<div @click="startVideo()" id="divClick">
			<img  id="imgFirstFrame" :src="require('./../../../images/' + pathToFirstFrame)" />
			<img  id="iconPlayVideo" src="./../../../images/iconPlayVideo.svg">
		</div>
		<span id="title">{{title}}</span>
		<span id="txt">{{text}}</span>
		<OpeningTag>Смотреть и голосовать</OpeningTag>
		<div @click="closeVideo(0)" v-show="controlsVisible" id="blockVideo">
			<video @click="closeVideo(1)" class="video" :id="`video${ID}`"  :src="require('./../../../assets/' + pathToVideo)" />
		</div>	
	</div>
</template>


<script >
import OpeningTag from './OpeningTag.vue'
export default {
	props: ['ID', 'title', 'text', 'pathToFirstFrame', 'pathToVideo'],
	data() {
		return {
			controlsVisible: false,
			tmp: 0,
		}
	},
	methods: {
		startVideo() {
			this.controlsVisible = true;
			var elem = document.getElementById(`video${this.ID}`);
			elem.play();
			elem.controls = true;
		},
		closeVideo(e) {
			console.log(e);
			if (e == 1) {
				this.tmp = 2;
			} else {
				this.tmp--;
			}
			if (!e && this.tmp <= 0) {
				var elem = document.getElementById(`video${this.ID}`);
				this.controlsVisible = false;
				elem.controls = false;
				elem.load();
			}
		}
	},
	components: {
		OpeningTag: OpeningTag
	},
}
</script>


<style scoped>

#divClick {
	position: relative;
} #divClick:hover #iconPlayVideo {
	transition: .2s;
	transform: scale(1.1, 1.1);
	opacity: 0.9;
}

#blockVideo {
	transition: 1s;
	display: flex;
	justify-content: center;
	top: 0px;
	left: 0px;
	position: absolute;
	z-index: 200;
	width: 100%;
	height: 100%;
	background-color: rgba(41, 41, 41, 0.589);
}

.video {
	transition: 1s;
	top: calc(50% - 194.5px);
	position: fixed;
	height: 445px;
	border-radius: 20px;
}

#bMain {
	margin-top: 32px;
	padding: 0px;
	display: flex;
	flex-direction: column;
	font-family: Arial;
	font-style: normal;
	width: fit-content;
}


#imgFirstFrame {
	width: 352px;
	height: 198px;
	border-radius: 16px;
}

#title{
	margin-top: 16px;
	font-weight: bold;
	font-size: 24px;
	line-height: 32px;
}

#txt {
	font-weight: normal;
	font-size: 16px;
	line-height: 24px;
}

#iconPlayVideo {
	position: absolute;
	top: calc(50% - 36px);
	left: calc(50% - 36px);
	width: 72px;
	height: 72px;
	opacity: 0.5;
}

@media (max-width: 1130px) {
	.video {
		top: calc(29%);
		width: 80%;
		height:auto;
	}
}

@media (max-width: 800px) {
	#imgFirstFrame {
		width: 300px;
		height: 170px;
	}
	.video {
		width: 90%;
	}
}

</style>