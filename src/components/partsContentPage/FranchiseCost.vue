<template>
	<div id="main">
		<div id="priceFranchise">Стоимость франшизы и цена владения</div>
		<div id="blockInfo">
			<div class="row">
				<span class="paragraph">Вступительный взнос</span>
				<span class="info">150 000 — 400 000 ₽</span>
			</div>
			<div class="row">
				<span class="paragraph">Роялти</span>
				<span class="info">5% от оборота в месяц, но не более 10 000 руб. При этом минимальная гарантированная сумма, подлежащая переводу Дилером, составляет 5 000 рублей (для городов менее 250 тысяч жителей 3 000 руб., для городов менее 100 тысяч согласовывается)</span>
			</div>
			<div class="row">
				<span class="paragraph">Иные текущие платежи</span>
				<span class="info">Аттестация и повышение квалификации тренеров 2 000 — 5 000 рублей в год</span>
			</div>
		</div>
		<hr id='hr'>
		<div id='downloadBlock'>
			<div id="imgDownload">
				<img id="img" src="./../../images/iconDownload.svg" />
			</div>
			<span :style="{'margin-left': '10px'}">Запросить финансовый план</span>
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

#main {
	display: block;
	border-radius: 16px;
	min-width: 232px;
	padding: 24px 0px 24px 0px;
	font-family: Arial;
	font-style: normal;
	background-color: rgba(30, 160, 30, 0.1);
}

#blockInfo {
	margin-top: 24px;
	margin-left: 24px;
} 

#priceFranchise {
	font-weight: bold;
	font-size: 24px;
	line-height: 32px;
	margin-left: 24px;
}

.paragraph {
	display: inline-block;
	font-weight: normal;
	font-size: 16px;
	line-height: 24px;
	color: rgba(0, 0, 0, 0.52);
	width: 200px;
	transition: .2s;
}

.row {
	display: flex;
	margin-top: 16px;
}

.info {
	transition: .2s;
	margin-left: 24px;
	width: 560px;
	font-weight: normal;
	font-size: 16px;
	line-height: 24px;
}

#hr {
	background: rgba(0, 0, 0, 0.2);
	border: 0px;
	height: 1px;
	width: 784px;
	width: 92%;
	margin-top: 24px;
}

#downloadBlock {
	font-weight: bold;
	font-size: 16px;
	line-height: 24px;
	display:  flex;
	justify-content: center;
	align-items: center;
	margin-top: 24px;
}

#imgDownload {
	border: 1px solid rgba(0, 0, 0, 0.52);
	border-radius: 25px;
	width: 24px;
	height: 24px;
	padding: 13px;
}

#imgDownload:hover #img{
	animation: jump 2s infinite;
}

@keyframes jump {
  0% {
		margin-top: 0px;
  }

  20% {
    margin-top: 10px;
  }
	40% {
    margin-top: 0px;
	}
	60% {
    margin-top: 10px;
	}
	100% {
    margin-top: 0px;
	}
}

@media (max-width: 1130px) {
	#priceFranchise {
		text-align: center;
	}
	.info {
		margin-left: 24px;
		width: 77.99%;
		font-weight: normal;
		font-size: 16px;
		line-height: 24px;
		margin-right: 1px;
	}
	#blockInfo {
		margin-top: 24px;
		margin-right: 24px;
	}
}

@media (max-width: 830px) {
	.row {
		display: flex;
		flex-direction: column;
	}
	.paragraph {
		margin-left: 24px;
	}
	.info {
		margin-top: 4px;
	}
	#priceFranchise {
		text-align: center;
		font-size: 18px;
		line-height: 24px;
	}
}

</style>