<template>
	<div class="header">
		<img class="iconLogo" src="./../images/iconBiBOSS.svg" />
		<div class="textLogo">БИБОСС</div>
		<div class="selected">
			<Selected :options="options" fontSize="16px"/>
		</div>
		<button class="btn">+ Объявление</button>
		<img class="iconMess" src="./../images/iconMess.svg" />
		<img class="iconNotification" src="./../images/iconNotification.svg" />
		<div class="blockPlusInactive">
			<span class="txtPlusInactive">ПЛЮС</span>
		</div>
		<div class="blockAvatar">
			<img class="photo" src="./../images/photoProfile.svg" />
			<span class="redCircle"></span>
			<div class="checkers">
				<div v-for="i in 5" :key="i" :style="getActive(i)"></div>
			</div>
		</div>
	</div>
</template>


<script>
import Selected from './Selected.vue'

export default {
	props: {},
	data() {
		return {
			options: [
				'Петропавловск-Камчатский', 'Киев', 'Казань', 'Набережные Челны', 'Елабуга' 
			]
		}
	},
	methods: {
		getActive(i) {
			let countActive = 2;
			let color = '#0D870D';
			let radiusLeft = 0;
			let radiusRight = 0;
			if (i == 1) {
				radiusLeft = 2;
			} else if (i == 5) {
				radiusRight = 2;
			}
			if (i > countActive) {
				color = 'rgba(0, 0, 0, 0.2)';
			}
			return ({
				'background-color': `${color}`,
				'width': '6px',
				'height': '4px',
				'margin-left': '1px',
				'border-top-left-radius': `${radiusLeft}px`,
				'border-bottom-left-radius': `${radiusLeft}px`,
				'border-top-right-radius': `${radiusRight}px`,
				'border-bottom-right-radius': `${radiusRight}px`,
			})
		}
	},
	components: {
			Selected: Selected,
	}
}
</script>


<style>
.header {
	display: flex;
	flex-direction: row;
	position: fixed;
	height: 56px;

	font-family: Arial;
	font-style: normal;
	font-weight: bold;
	box-shadow: 3px 0px 10px #FA961E;
}

.iconLogo {
	position: relative;
	display: inline-block;
	width: 24px;
	height: 24px;
	top: calc(50% - 24px / 2 - 0px);
	left: 2.3%;
}

.textLogo {
	font-size: 24px;

	display: inline;
	position: relative;
	width: 106px;
	height: 24px;
	/* left: 48px; */
	left: 3.35%;
	top: calc(50% - 24px/2 - 0px);
}

.selected {
	height: 24px;
	top: calc(50% - 24px/2 - 0px);
	display: inline-block;
	position: relative;
	left: 98px;
	left: 6.85%;
	/* width: 260px; */
}

.btn {
	position: relative;
	top: calc(50% - 42px / 2 - 0px);
	/* left: 140px; */
	widows: 139px;
	height: 42px;

	font-size: 16px;
	line-height: 24px;

	color: #fff;
	background-color: #0D870D;

	border-radius: 6px;
	border: 2px solid rgba(0, 0, 0, 0);
	transition: 0.2s
}.btn:hover {
	transform: translateY(-1px);
	border: 2px solid #0D870D;
	background-color: #fff;
	color: #0D870D;
}

.iconMess {
	width: 24px;
	height: 24px;
	position: relative;
	top: calc(50% - 24px/ 2 - 0px)
}

.iconNotification {
	width: 24px;
	height: 24px;
	position: relative;
	top: calc(50% - 24px/ 2 - 0px)
}

.blockPlusActive {
	position: relative;
	top: calc(50% - 28px/ 2 - 0px);
	width: 66px;
	height: 28px;
	background-color: #FA961E;
	border-radius: 36px; 
}

.txtPlusActive {
	display: flex;
	position: relative;
	top: calc(50% - 22px/ 2 - 0px);
	left: 13px;
	width: 50px;
	height: 21px;
	background-color: #fff;
	color: #FA961E;
	border-radius: 36px;

	padding-top: 1.2px;
	justify-content: center;

	font-family: Arial;
	font-style: normal;
	font-weight: bold;
	font-size: 12px;
	line-height: 20px;
}

.blockPlusInactive {
	position: relative;
	top: calc(50% - 28px/ 2 - 0px);
	width: 66px;
	height: 28px;
	background-color:  rgba(0, 0, 0, 0.2);
	border-radius: 36px; 
}

.txtPlusInactive {
	display: flex;
	position: relative;
	top: calc(50% - 22px/ 2 - 0px);
	left: 3px;
	width: 50px;
	height: 21px;
	background-color: #fff;
	color:  rgba(0, 0, 0, 0.2);
	border-radius: 36px;

	padding-top: 1.2px;
	justify-content: center;

	font-family: Arial;
	font-style: normal;
	font-weight: bold;
	font-size: 12px;
	line-height: 20px;
}

.blockAvatar {
	width: 64px;
	height: 56px;
	position: relative;
}

.photo {
	width: 32px;
	height: 32px;
	position: relative;
	top: 8px;
	left: 16px;
	border-radius: 100px;
}

.redCircle {
	display: block;
	position: absolute;
	width: 8px;
	height: 8px;
	border-radius: 8px;
	background-color: rgba(237, 47, 47, 1);

	top: 8px;
	left: 40px;
}

.checkers {
	display: flex;
	position: relative;
	top: 6px;
	left: 14px;
	width: 35px;
	height: 4px;
}
</style>