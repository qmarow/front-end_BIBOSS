<template>
	<div id="main">
		<TitleWithHR>О компании</TitleWithHR>
		<div>
			<p>Открой СВОЙ БИЗНЕС на услугах рабочей силы и ЗАРАБАТЫВАЙ от 200 000 рублей в месяц.</p>
			<p>За руку доведем до 200 000 руб/ мес личного дохода, даже если это твой первый бизнес!</p>
			<p>- НАЧАТЬ ОЧЕНЬ ЛЕГКО</p>
			Без найма кучи народу, закупок, оборудования и “закапывания” миллионов на годы. Первое время можно без офиса.
		</div>
		<OpeningTag>Страница франшизы</OpeningTag>
		<div id="franchiceCost">
			<FranchiceCost />
		</div>
		<div id="franchiseDescription">
			<FranchiseDescription />
		</div>
		<div id="blockImages">
			<img v-for="(src, i) in srcImages" :key="i" class="imagesFranchise" :src="require('./../../images/' + src)"/>
		</div>
		<div>
			<AgentCard />
		</div>
	</div>
</template>


<script>
import FranchiceCost from './FranchiseCost.vue'
import TitleWithHR from './auxiliaryElements/TitleWithHR.vue'
import FranchiseDescription from './FranchiseDescription.vue'
import OpeningTag from './auxiliaryElements/OpeningTag.vue'
import AgentCard from './AgentCard.vue'
export default {
	props: {},
	data() {
		return {
			srcImages: ['firstExample.jpg', 'secondExample.jpg', 'thirdExample.jpg', 'fourthExample.jpg']
		}
},
	components: {
		FranchiceCost: FranchiceCost,
		TitleWithHR: TitleWithHR,
		FranchiseDescription: FranchiseDescription,
		OpeningTag: OpeningTag,
		AgentCard: AgentCard,
	}
}
</script>


<style scoped>

#main {
	width: 832px;
	background-color: rgba(46, 114, 44, 0.637);
	font-family: Arial;
	font-style: normal;
}

.boldText {
	font-weight: bold;
	font-size: 24px;
	line-height: 32px;
}

.imagesFranchise {
	margin-left: 16px;
	width: 196px;
	height: 196px;
	border-radius: 16px;
	transition: .2s;
} 
.imagesFranchise:first-child {
	margin-left: 0px;
}

#franchiceCost {
	margin: 0px;
	margin-top: 32px;
}

#blockImages {
	margin-top: 32px;
	width: 100%;
	display: inline-block;
	transition: .2s;
}

#blockImages::-webkit-scrollbar {
  /* width: 6px; */
	height: 0px;
  background-color: #ffffff;
  border-radius: 10px;
	margin-bottom: 6px;
}
#blockImages:nth-child(2) {
	width: 10px;
}

#blockImages::-webkit-scrollbar-thumb {
  display: block;
	border-radius: 10px;
  background-color: #73ff66c9;
}

#blockImages::-webkit-scrollbar-track {
  /* -webkit-box-shadow: inset 0 0 3px rgba(0,0,0,0.2); */
  /* border-radius: 100px;
  background-color: #606061;
	height: 10px; */
}

#franchiseDescription {
	margin-top: 32px;
}

@media (max-width: 1130px) {
	#main {
		width: 100%;
	}
	#franchiceCost {
		margin-left: 0%;
	}
	.imagesFranchise {
		margin-left: 2%;
		width: 23%;
		height: 23%;
		border-radius: 16px;
	}
	.imagesFranchise:first-child {
		margin-left: 1%;
	}
}

@media (max-width: 830px) {
	#blockImages {
		text-align: center;
		margin-top: 24px;
		width: 100%;
		display: inline-block;
		/* height: 220px; */
		overflow: auto;
	}
	.imagesFranchise {
		/* background-color: brown; */
		margin: 0px;
		padding: 4px;
		padding-top: 4px;
		padding-bottom: 0px;
		width: 167px;
		height: 167px;
		border-radius: 8px;
	}
}

</style>