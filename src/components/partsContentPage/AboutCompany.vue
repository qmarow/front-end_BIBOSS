<template>
	<div id="main">
		<div class="boldText">О компании</div>
		<hr/>
		<div>
			<p>Открой СВОЙ БИЗНЕС на услугах рабочей силы и ЗАРАБАТЫВАЙ от 200 000 рублей в месяц.</p>
			<p>За руку доведем до 200 000 руб/ мес личного дохода, даже если это твой первый бизнес!</p>
			<p>- НАЧАТЬ ОЧЕНЬ ЛЕГКО</p>
			Без найма кучи народу, закупок, оборудования и “закапывания” миллионов на годы. Первое время можно без офиса.
		</div>
		<div :style="{'display': 'flex', 'font-size': '16px', 'line-height': '24px', 'margin-top': '16px'}" class="boldText">
			Страница франшизы
			<img :style="{'margin-left': '5px'}" src="./../../images/iconMiniArrawRight.svg"/>
		</div>
		<div :style="{'margin-top': '32px'}">
			<FranchiceCost />
		</div>
	</div>
</template>


<script>
import FranchiceCost from './FranchiseCost.vue'
export default {
	props: {},
	data() {
		return {}
},
	components: {
		FranchiceCost: FranchiceCost
	}
}
</script>


<style scoped>

#main {
		width: 832px;
		/* width: 58.9%; */
		/* background-color: blueviolet; */
		font-family: Arial;
		font-style: normal;
}

.boldText {
		font-weight: bold;
		font-size: 24px;
		line-height: 32px;
}

</style>