<template>
	<div class="mainBlock">
		<div class="medalBlock">
			<img src="./../../images/medal.svg" />
			<div class="textsMedal">
				<span :style="{'font-weight': 'normal'}">Конкурс БИБОСС</span>
				<span :style="{'font-weight': 'bold'}">«Лучшее видео о франшизе»</span>
			</div>
		</div>
		<div id="textPersonalSolution">Видео о франшизе «Персональное решение»</div>
		<div id="blockVideoColumnVote">	
			<div id="blockVideo">
				<video id="videoMedia" src="./../../assets/FranchiseVideo.mp4" preload="auto" poster="./../../images/firstCadr.jpg"/>
				<img @click="startVideo()" src='./../../images/iconPlayVideo.svg' id="btnPlay" :class="controlsVisible == true ? 'btnPlayOff' : 'btnPlayOn'" />
				<div @click="closeVideo()" v-if="controlsVisible" class='close-btn'>
					<span></span>
				</div>
			</div>
			<div id='columnVote'>
				<span class="txtVote">Голосование</span>
				<p class="txtVote">Для того, чтобы проголосовать за видео, нужно сделать репост в любой из соцсетей:</p>
				<div id="btnSocialNet">
					<a href="https://ru-ru.facebook.com/" :style="{'background-color': 'rgba(31, 59, 116, 1)'}" class="vote">
						<img src="./../../images/iconFB.svg" />
						<div class="voteTxt">Голосовать FB</div>
					</a>
					<a href="https://vk.com/im?peers=442227683_178451614" :style="{'background-color': 'rgba(39, 70, 106, 1)'}" class="vote">
						<img src="./../../images/iconVK.svg" />
						<div class="voteTxt">Голосовать VK</div>
					</a>
					<a href="" :style="{'background-color': 'rgba(208, 99, 19, 1)'}" class="vote">
						<img src="./../../images/iconOK.svg" />
						<div class="voteTxt">Голосовать OK</div>
					</a>
				</div>
				<div id="countVote">657 голосов</div>
			</div>
		</div>
	</div>
</template>


<script>
export default {
	props: {},
	inject: ['width'],
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
	padding: 0px;
}

.medalBlock {
	top: 28px;
	position: relative;
	display: flex;
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
	font-family: Arial;
	font-style: normal;
	font-weight: bold;
	margin-top: 48px;
	font-size: 48px;
	display: flex;
	align-items: center;
	text-align: center;
	justify-content: center;
}

#blockVideo {
	margin-top: 36px;
	position: relative;
	display: inline-block;
}

#videoMedia {
	width: 832px;
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

.close-btn {
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
}.close-btn:hover {
	border: 2px solid rgb(196, 196, 196);

}.close-btn span::before,
.close-btn span::after{
	border-radius: 10px;
	width: 15px;
	height: 2px;
	background-color: rgb(196, 196, 196);
	position: absolute;
	top: 50%; margin-top: -1px;
	left: calc(50% - 7.5px);
}.close-btn span::before {
	transform: rotate(-45deg);
}.close-btn span::after {
	transform: rotate(45deg);
}.close-btn span::before,
.close-btn span::after {
	content: '';
	display: block;
	transition: 0.1s;
}.close-btn:hover span::after {
	width: 12px;
	left: calc(50% - 6px);
}.close-btn:hover span::before {
	width: 12px;
	left: calc(50% - 6px);
}

#columnVote {

	margin-top: 46px;
	margin-left: 10px;
	width: 256px;
	font-family: Arial;
	font-style: normal;
} #columnVote span {
	font-weight: bold;
	font-size: 24px;
	line-height: 32px;
} #columnVote p {
	font-weight: normal;
	font-size: 16px;
	line-height: 24px;
}



.voteTxt {
	margin-top: 20px;
	padding: 0px;
	display: inline-block;
	font-weight: bold;
	font-size: 18px;
	line-height: 24px;
	margin-left: 15px;
	color: #fff;
}

.vote {
	margin-top: 8px;
	display: flex;
	border-radius: 30px;
	height: 60px;
	text-decoration: none;
}

#countVote {
	font-family: Arial;
	font-style: normal;
	font-weight: bold;
	font-size: 18px;
	line-height: 24px;
	margin-top: 10px;
	display: flex;
	justify-content: center;
}

#blockVideoColumnVote {
	display: flex;
	flex-direction: row;
}

@media (max-width: 1130px) {
	.mainBlock {
		padding: 0px 16px;
	}

	#blockVideoColumnVote {
		flex-direction: column;
	}
	#blockVideo {
		display: flex;
		justify-content: center;
	}
	#videoMedia {
		width: 100%;
	}
	#columnVote {
		margin-top: 32px;
		width: 100%;
		margin-left: 0px;
	}
	#btnSocialNet {
		display: flex;
		justify-content: space-evenly;
	}

	.vote {
		width: 256px;
	}

	.txtVote {
		display: flex;;
		justify-content: center;
		text-align: center;
	}

	#textPersonalSolution {
		font-size: 36px;
	}
}

@media (max-width: 830px) {
	.voteTxt {
		display: none;
		width: 24px;
	}

	.vote {
		width: 60px;
		margin-right: 8px;
	}
	#btnSocialNet {
		/* display: flex; */
		justify-content: center;
	}
	#textPersonalSolution {
		font-family: Arial;
		font-style: normal;
		font-weight: bold;
		font-size: 24px;
		line-height: 32px;
		/* or 133% */

		display: flex;
		align-items: center;
		text-align: center;
	}
	.close-btn {
		left: 94%;
	}
}

</style>