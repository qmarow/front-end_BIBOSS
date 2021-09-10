<template>
	<div>
		<div @click="active = !active" :style="{'display': 'flex', 'font-size': '16px', 'line-height': '24px', 'margin-top': '16px'}" class="boldText">
			<slot />
			<div class='menu-btn' :class="active ? 'menu-btn-1' : ''">
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
			active: false,
		}
},
	components: {}
}
</script>


<style scoped>

.boldText {
		font-weight: bold;
		font-size: 24px;
		line-height: 32px;
}


.menu-btn {
	margin-top: 2.5px;
	margin-left: 7px;
	display: block;
	width: 20px;
	height: 20px;
	border-radius: 50%;
	position: relative;
}

.menu-btn span,
.menu-btn span::before,
.menu-btn span::after 
{
	border-radius: 10px;
	/* width: 10.5px; */
	height: 2px;
	background-color: rgb(196, 196, 196);
	position: absolute;
	top: 50%; margin-top: -1px;
	left: 50%; margin-left: -2px;
}
.menu-btn span::before {
	margin-top: -4px;
	transform: rotate(45deg);
}.menu-btn span::after 
{
	margin-top: 2px;
	transform: rotate(-45deg);
}.menu-btn span::before,
.menu-btn span::after {
	width: 10.5px;
	content: '';
	display: block;
	transition: 0.1s;
}

.menu-btn-1 span {
	height: 1.5px;
	width: 14px;
	left: 50%; margin-left: -7px;
}

.menu-btn-1 span::before {
	height: 1.8px;
	left: 50%; margin-left: -7px;
	transform: rotate(0deg) translateY(-0.5px);
	width: 14px;
}.menu-btn-1 span::after {
	height: 1.8px;
	left: 50%; margin-left: -7px;
	transform: rotate(0deg) translateY(0.5px);
	width: 14px;
}

</style>