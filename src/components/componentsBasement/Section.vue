<template>
	<div>
		<div id="title">Разделы</div>
		<div class="line">
			<img src="./../../images/iconPeople.svg"/>
			<span>Сообщение</span>
		</div>
		<div class="line">
			<img src="./../../images/iconKN.svg">
			<span>Коммерческая недвижимоть</span>
		</div>
		<div class="line">
			<img src="./../../images/iconFD.svg">
			<span class=''>Франшизы</span>
		</div>
		<div class="line">
			<img src="./../../images/iconGB.svg">
			<span>Готовый бизнес</span>
		</div>
		<div class="line">
			<img id="img" src="./../../images/iconOpt.svg">
			<span>Товары и услуги</span>
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

#id title{
	font-weight: bold;
	font-size: 14px;
	line-height: 20px;
	color: #FFFFFF;
	opacity: 0.6;
}

</style>