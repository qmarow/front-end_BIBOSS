<template>
	<div class="header">
		<div id="left-part-header">
			<a @click="$emit('changeBar')" class="menu-btn-bar" :class="visibleBar ? 'menu-btn-bar_active' : ''">
				<span></span>
			</a>
			<img class="iconLogo" src="./../images/iconBiBOSS.svg" />
			<div class="textLogo">БИБОСС</div>
			<div class="selected">
				<Selected :options="options" fontSize="16px"/>
			</div>
		</div>
		<div id="right-part-header">
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
			<div id="entrance">
				<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path d="M15 7C15 5.34314 13.6569 4 12 4C10.3431 4 9 5.34314 9 7C9 8.65686 10.3431 10 12 10C13.6569 10 15 8.65686 15 7ZM17 7C17 9.76143 14.7614 12 12 12C9.23857 12 7 9.76143 7 7C7 4.23858 9.23857 2 12 2C14.7614 2 17 4.23858 17 7ZM21 18.9283C21.122 20.6085 19.7389 22 18.0507 22L5.95681 22C4.26854 22 2.88548 20.6085 3.0075 18.9283C3.28678 15.0828 7.26692 13 12.0001 13C16.7239 13 20.7183 15.0499 21 18.9283ZM19.005 19.0732C18.7951 16.1819 15.6055 15 11.9998 15C8.37245 15 5.20898 16.2238 5.00204 19.0732C4.96645 19.5633 5.4005 20 5.95661 20L18.0505 20C18.6066 20 19.0406 19.5633 19.005 19.0732Z" fill="black" fill-opacity="0.2"/>
				</svg>
				<span>Войти</span>
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

#left-part-header {
	display: flex;
	float: left;
	height: 56px;
}

#right-part-header {
	display: flex;
	justify-content: right;
}

.header {
	height: 56px;
	width: 100%;

	font-family: Arial;
	font-style: normal;
	font-weight: bold;
	box-shadow: 1px 1px 10px #85858523;
}

.iconLogo {
	display: inline-block;
	width: 24px;
	height: 24px;
	margin-top: 16px;
	margin-left: 1%;
	top: calc(50% - 24px / 2 - 0px);
}

.textLogo {
	display: inline-block;
	font-size: 24px;
	width: 106px;
	height: 24px;
	margin-left: 0.54%;
	margin-top: 14px;
}

.selected {
	display: inline-block;
	height: 24px;
	margin-left: 32px;
	width: 239px;
	min-width: 239px;
	margin-top: 17px;
}

.btn {
	margin-top: 6px;
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
	/* float: right; */
	margin-left: 23px;
	width: 24px;
	height: 24px;
	margin-top: 16px;
	transition: 0.1s;
}.iconMess:hover {
	transform: translateY(-3px);
}

.iconNotification {
	margin-left: 23px;
	width: 24px;
	height: 24px;
	margin-top: 16px;
	transition: 0.1s;
}.iconNotification:hover {
	transform: translateY(-3px);
}

.blockPlus {
	display: inline-block;
	margin-left: 23px;
	margin-top: 14px;
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
	display: inline-block;
	width: 64px;
	height: 56px;
	margin-right: 1px;
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

#entrance {
	display: none;
	height: 56px;
	align-items: center;
	margin-left: 10px;
} #entrance span {
	font-weight: normal;
	font-size: 14px;
	line-height: 20px;
	margin: 0px 8px;
}

.menu-btn-bar {
	left: 1px;
	top: calc(50% - 20px);
  display: inline-block;
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

@media (max-width: 850px) {
	.selected {
		display: none;
	}
	.btn {
		display: none;
	}
}

@media (max-width: 530px) {
	.textLogo {
		display: none;
	}
	.blockAvatar {
		display: none;
	}
	.iconMess {
		display: none;
	}
	.iconNotification {
		display: none;
	}
	#entrance {
		display: flex;
	}
}

</style>