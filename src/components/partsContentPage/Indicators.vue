<template>
	<div id="main">
		<div :style="{'font-weight': 'bold', 'font-size': '24px', 'line-height': '32px'}">Показатели</div>
		<hr />
		<div class="number">1720</div>
		<div class="txt">Год основания компании</div>
		<div class="number">1894</div>
		<div>Год запуска франчайзинга</div>
		<div class="number">26 850</div>
		<div>Год запуска франчайзинга</div>
		<div class="number">1</div>
		<div>Собственных предприятий</div>

	</div>
</template>


<script>
export default {
	props: {},
	data() {
		return {}
},
	components: {}
}
</script>


<style scoped>

#main {
	font-family: Arial;
	font-style: normal;
	width: 256px;
	height: 305px;
}

.number {
	margin-top: 16px;
	font-weight: bold;
	font-size: 18px;
	line-height: 24px;
}

.txt {
	font-weight: normal;
	font-size: 16px;
	line-height: 24px;
}

hr {
	width: 256px;
	border: 0px;
  height: 1px;
  background-color: rgba(0, 0, 0, 0.2);;
}

</style>