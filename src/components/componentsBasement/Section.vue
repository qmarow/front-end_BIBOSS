<template>
	<div>
		<div id="title">РАЗДЕЛЫ</div>
		<div class="line">
			<img src="./../../images/iconPeople.svg"/>
			<span class="txtInBasmentColumns">Сообщение</span>
		</div>
		<div class="line">
			<img src="./../../images/iconKN.svg">
			<span class="txtInBasmentColumns">Коммерческая недвижимоть</span>
		</div>
		<div class="line">
			<img src="./../../images/iconFD.svg">
			<span class="txtInBasmentColumns">Франшизы</span>
		</div>
		<div class="line">
			<img src="./../../images/iconGB.svg">
			<span class="txtInBasmentColumns">Готовый бизнес</span>
		</div>
		<div class="line">
			<img id="img" src="./../../images/iconOpt.svg">
			<span class="txtInBasmentColumns">Товары для бизнеса</span>
		</div>

		<div class="line">
			<img id="img" src="./../../images/iconInvest.svg">
			<span class="txtInBasmentColumns">Инвестпроекты</span>
		</div>
		<div class="line">
			<img id="img" src="./../../images/iconIdea.svg">
			<span class="txtInBasmentColumns">Бизнес-идеи</span>
		</div>
		<div class="line">
			<img id="img" src="./../../images/iconBPlan.svg">
			<span class="txtInBasmentColumns">Бизнес-планы</span>
		</div>
		<div class="line">
			<img id="img" src="./../../images/iconApplications.svg">
			<span class="txtInBasmentColumns">Заявки</span>
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