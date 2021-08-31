<template>
	<div class="select">
		<div  @click="visible(null)"  class="selectBlock">	
			<div :style="{'font-size': fontSize}" class="selectTxt">{{selectedComponent}}</div>
			
			<div class='menu-btn' :class="change ? 'menu-btn-1' : ''">
				<span></span>
			</div>
		</div>
		<transition name='list'>
			<div v-show="isVisible != 2" class="optionsBlock">
				<transition name='opt'  v-for='(elem, i) in options' :key="i">
					<p v-show="optIndetifier[i]" @click="visible(elem)" :style="{'font-size': fontSize}" class="option">{{elem}}</p>
				</transition>
			</div>
		</transition>
	</div>
</template>


<script>
export default {
	props: {
			options: {
					type: Array,
					// default: null,
			},
			fontSize: {
				type: String, 
				// default: '110px',
			},
	},
	mounted() {
		for (var i = 0; i < this.options.length; i++) {
			this.optIndetifier[i] = false;
		}
		console.log(this.optIndetifier)
	},
	data() {
		return {
				selectedComponent: (this.options == null) ? null : this.options[0],
				isVisible: 2,
				change: false,
				optIndetifier: [],
		}
	},
	watch: {
		isVisible: function() {
			if (this.isVisible == 0) {
				for (let i = 1; i - 1 < this.optIndetifier.length; i++) {
					setTimeout(() => {
						this.optIndetifier[i - 1] = true;
					}, i * 25)
				}
			} else if (this.isVisible == 1){
				setTimeout(() => {
					console.log('!!!!!!');
					this.isVisible = 2;
					}, 20 * this.optIndetifier.length)
				for (let i = 1; i < this.optIndetifier.length + 1; i++) {
					((j) => {
						setTimeout(() => {
							this.optIndetifier[this.optIndetifier.length - j] = false;
						}, j * 20)
					})(i)
				}
			}
		},
	},
	methods: {
		visible(elem) {
			if (elem !== null) {
				console.log(elem);
				this.selectedComponent = elem;
			}
			this.change = !this.change;
			if (this.isVisible == 0) {
				this.isVisible = 1;
			} else if (this.isVisible == 2) {
				this.isVisible = 0;
			}
		}
	},
	components: {}
}
</script>


<style  scoped>

.menu-btn {
	margin-left: 7px;
	display: block;
	width: 20px;
	height: 20px;
	/* background-color: rgb(228, 119, 119); */
	border-radius: 50%;
	position: relative;
}

/* .menu-btn span, */

.menu-btn span::before,
.menu-btn span::after 
{
	border-radius: 10px;
	width: 10.5px;
	height: 2px;
	background-color: rgb(196, 196, 196);
	position: absolute;
	top: 50%; margin-top: -1px;
}

.menu-btn span::before
{
	transform: rotate(-45deg);
	right: 50%; margin-right: -8.4px;
}
.menu-btn span::after 
{
	transform: rotate(45deg);
	left: 50%; margin-left: -8.4px;
}

.menu-btn span::before,
.menu-btn span::after {
	content: '';
	display: block;
	transition: 0.1s;
}

.menu-btn-1 span::before {
	transform: rotate(45deg);
	width: 10.5px;
	/* transform-origin: right top; */
}
.menu-btn-1 span::after {
	transform: rotate(-45deg);
	width: 10.5px;
	/* transform-origin: left top; */
}

.select {
	/* display: inline-block; */
	font-family: Arial;
	font-style: normal;
	font-weight: normal;
}

.optionsBlock {
	border: 1px solid rgb(199, 199, 199);
	border-radius: 10px;
	background-color: rgb(255, 255, 255);
	width: 100%;
	padding: 0px 0px;
	transition: 0.8s;
}

.option {
	display: inline-block;
	margin: 2.5% 1%;
	color: #070707;
	/* line-height: 2em; */
	padding: 4px 0.5em;
  overflow: hidden;
	transition: 0.2s;
}.option:hover {
	transform: translateX(5px);
	background-color: rgba(255, 218, 11, 0.301);
}


.selectBlock {
	display: inline-flex;
	align-items: center;
	border: 1px solid rgba(179, 89, 89, 0);
	padding: 0px 3px;
	border: 2px solid #ffffff00;
		border-top-width: 0px;
	border-right-width: 0px;
	border-left-width: 0px;
	/* width: 100px; */
}

.selectBlock:hover {

}

.imgBlock {
	display: flex;
	/* float: right; */
	/* margin-left: 2.8%; */
	padding-left: 5.36px;
	/* margin-top: 5.36px; */
	/* position: relative; */
	align-items: center;
	/* background-color: slategrey; */
	width: 20px;
	height: 20px;
}

.img {
	width: 24px;
	height: 24px;
}

.list-leave-active {
	transition: 0.1s;
	opacity: 0;
}

.opt-enter-active {
	transition: 0.1s;
	opacity: 0;
	/* background: rgb(34, 129, 173); */
	transform: translateY(-10px);
}

.opt-leave-active {
	transition: 0.1s;
	opacity: 0;
	/* background: rgb(34, 129, 173); */
	transform: translateY(-10px);
}

</style>