<template>
	<div class="header">
		<a @click="$emit('changeBar')" class="menu-btn-bar" :class="visibleBar ? 'menu-btn-bar_active' : ''">
			<span></span>
		</a>
		<img class="iconLogo" src="./../images/iconBiBOSS.svg" />
		<div class="textLogo">БИБОСС</div>
		<div class="selected">
			<Selected :options="options" fontSize="16px"/>
		</div>
		<button class="btn">+ Объявление</button>
		<img class="iconMess" src="./../images/iconMess.svg" />
		<img class="iconNotification" src="./../images/iconNotification.svg" />
		<div class="blockPlus" :class="getActiveBlockPlus">
			<span class="txtPlus" :class="getActiveTextPlus">ПЛЮС</span>
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
	props: ['visibleBar'],
	emits: ['changeBar'],
	data() {
		return {
			options: [
				'Петропавловск-Камчатский', 'Киев', 'Казань', 'Набережные Челны', 'Елабуга' 
			],
			blockPlusActive: true,
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
	computed: {
		getActiveBlockPlus() {
			if (this.blockPlusActive) {
				return 'BPActive';
			} else {
				return 'BPInactive';
			} 
		},
		getActiveTextPlus() {
			if (this.blockPlusActive) {
				return 'TPActive';
			} else {
				return 'TPInactive';
			} 
		},
	},
	components: {
			Selected: Selected,
	}
}
</script>


<style scoped>
.header {
	display: flex;
	flex-direction: row;
	height: 56px;
	width: 100%;

	font-family: Arial;
	font-style: normal;
	font-weight: bold;
	box-shadow: 1px 1px 10px #85858523;
}

.iconLogo {
	position: relative;
	/* display: inline; */
	width: 24px;
	height: 24px;
	top: calc(50% - 24px / 2 - 0px);
	/* margin-left: 0.1%; */
}

.textLogo {
	font-size: 24px;

	/* display: inline; */
	position: relative;
	width: 106px;
	height: 24px;
	margin-left: 0.54%;
	top: calc(50% - 24px/2 - 0px);
}

.selected {
	height: 24px;
	top: calc(50% - 24px/2 - 0px);
	/* display: inline-block; */
	position: relative;
	margin-left: 2.1%;
	width: 19%;
	min-width: 240px;
}

.btn {
	position: relative;
	top: calc(50% - 42px / 2 - 0px);
	margin-left: 36.3%;
	left: 0%;
	min-width: 139px;
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
	margin-left: 2.1%;
	width: 24px;
	height: 24px;
	position: relative;
	top: calc(50% - 24px/ 2 - 0px);
	transition: 0.1s;
}.iconMess:hover {
	transform: translateY(-3px);
}

.iconNotification {
	margin-left: 2.1%;
	width: 24px;
	height: 24px;
	position: relative;
	top: calc(50% - 24px/ 2 - 0px);
	transition: 0.1s;
}.iconNotification:hover {
	transform: translateY(-3px);
}

.blockPlus {
	margin-left: 2.1%;
	position: relative;
	top: calc(50% - 28px/ 2 - 0px);
	min-width: 66px;
	height: 28px;
	border-radius: 36px; 
}

.BPActive {
	background-color: #FA961E;
}

.BPInactive {
	background-color:  rgba(0, 0, 0, 0.2);
}

.txtPlus {
	display: flex;
	position: relative;
	top: calc(50% - 22px/ 2 - 0px);
	width: 50px;
	height: 21px;
	border-radius: 36px;

	padding-top: 1.2px;
	justify-content: center;

	font-family: Arial;
	font-style: normal;
	font-weight: bold;
	font-size: 12px;
	line-height: 20px;
}

.TPActive {
	left: 13px;
	color: #FA961E;
	background-color: #fff;
}

.TPInactive {
	left: 3px;
	color:  rgba(0, 0, 0, 0.2);
	background-color: #fff;
}

.blockAvatar {
	margin-left: 1.05%;
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

.menu-btn-bar {
	top: calc(50% - 20px);
  display: block;
  width: 40px;
  height: 40px;
  /* background-color: rgb(252, 126, 126); */
  /* border-radius: 50%; */
  position: relative;
}
.menu-btn-bar span,
.menu-btn-bar span::before,
.menu-btn-bar span::after {
  position: absolute;
  top: 50%; margin-top: -1px;
  left: 50%; margin-left: -9px;
  width: 18px;
  height: 2px;
  background-color: rgb(197, 197, 197);
	transition: .1s;
}
.menu-btn-bar span::before,
.menu-btn-bar span::after {
	transition: 0.2s;
  content: '';
  display: block;
}
.menu-btn-bar span::before {
  transform: translateY(-6px);
}
.menu-btn-bar span::after {
  transform: translateY(6px);
}

.menu-btn-bar_active span {
	width: 0px;
	margin-left: 0%;
}

.menu-btn-bar_active span:before {
	transition: 0.2s;
	transform: rotate(-135deg);
  width: 20px;
}
.menu-btn-bar_active span:after {
	transition: 0.2s;
  transform:  rotate(135deg);
  width: 20px;
}

</style>