<template>
	<div class="header">
		<img class="iconLogo" src="./../images/iconBiBOSS.svg" />
		<div class="textLogo">БИБОСС</div>
		<div class="selected">
				<Selected :options="options" fontSize="16px"/>
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
	background-color: red;
	height: 56px;

	font-family: Arial;
	font-style: normal;
	font-weight: bold;
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

</style>