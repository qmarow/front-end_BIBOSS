<template>
	<div>
		<div id="title">СОЦСЕТИ</div>
		<div class="line">
			<img src="./../../images/iconPeople.svg"/>
			<span class="txtInBasmentColumns">Facebook</span>
		</div>
		<div class="line">
			<img src="./../../images/iconKN.svg">
			<span class="txtInBasmentColumns">Вконтакте</span>
		</div>
		<div class="line">
			<img src="./../../images/iconFD.svg">
			<span class="txtInBasmentColumns">Телеграм</span>
		</div>
		<div class="line">
			<img src="./../../images/iconGB.svg">
			<span class="txtInBasmentColumns">Instagramm</span>
		</div>
		<div class="line">
			<img id="img" src="./../../images/iconOpt.svg">
			<span class="txtInBasmentColumns">Youtube</span>
		</div>

		<div class="line">
			<img id="img" src="./../../images/iconInvest.svg">
			<span class="txtInBasmentColumns">Одноклассники</span>
		</div>
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

img.img  svg{
	vertical-align: middle;
    stroke: #fcc10a;
    stroke-width: 2px;
    fill: #fff;
}

#title{
	font-weight: bold;
	font-size: 14px;
	line-height: 20px;
	color: #FFFFFF;
	opacity: 0.6;
	margin-left: 4px;
	margin-top: 24px;
}

</style>