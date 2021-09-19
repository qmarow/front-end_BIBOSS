<template>
  <div id="main">
		<div id="blockPhotoInfo">
			<div id="blockPhotoInfo2">
				<div id="photoNetJobForce">
					<img src="./../../images/photoNetJobForce.svg" />
				</div>
				<div id="info">
					<span id="personalSolution" >Персональное решение</span>
					<span id="investments" >Инвестиции 378 000 — 675 000 ₽</span>
					<div id="pageFranchise">
						<span>Страница франшизы</span>
						<img :style="{'margin-left': '8px', 'display': 'flex'}" src="./../../images/iconMiniArrawRight.svg" />
					</div>	
				</div>
			</div>
		</div>
		<hr id="hr">
		<div id="blockAgentMain">
			<div id="blockAgent">
				<BlockAgent />
				<div>
					<button id="btnRequestPhinplan">Запросить финплан</button>
				</div>
			</div>
		</div>
  </div>
</template>


<script>
import BlockAgent from './auxiliaryElements/BlockAgent.vue'
export default {
  props: {},
  data() {
	return {}
},
  components: {
	BlockAgent: BlockAgent,
  }
}
</script>


<style scoped>

#main {
	width: 1120px;
	height: 162px;
	background: #FFFFFF;
	box-shadow: 0px 10px 40px rgba(0, 0, 0, 0.15);
	border-radius: 16px;
	transition: .2s;
}

#photoNetJobForce {
	display: flex;
	transition: .2s;
}

#info {
	margin-top: 8px;
	margin-left: 32px;
	display: inline-block;
	font-family: Arial;
	font-style: normal;
	transition: .2s;
}

#personalSolution {
	display: block;
	font-weight: bold;
	font-size: 24px;
	line-height: 32px;
	transition: .2s;

}

#investments {
	display: block;
	margin-top: 8px;
	font-weight: normal;
	font-size: 16px;
	line-height: 24px;
	transition: .2s;
}

#pageFranchise {
	transition: .2s;

	display: flex;
	margin-top: 8px;
	font-weight: bold;
	font-size: 16px;
	line-height: 24px;
}


#btnRequestPhinplan {
	margin-top: 16px;
	background-color: #0D870D;
	border: 2px solid #ffffff00;
	border-radius: 6px;
	width: 232px;
	height: 46px;
	color: #FFFFFF;
	font-family: Arial;
	font-style: normal;
	font-weight: bold;
	font-size: 16px;
	line-height: 24px;
	transition: 0.2s;
} #btnRequestPhinplan:hover {
	transform: translateY(-1px);
	background-color: #ffffff;
	color: #0D870D;
	border: 2px solid #0D870D;

}

#blockAgent {
	transition: .2s;

	margin-top: 24px;
	display: flex;
	flex-direction: column;
}

#blockAgentMain {
	transition: .2s;

	margin-right: 24px;
	display: flex;
	justify-content: right;
}

#blockPhotoInfo {
	transition: .2s;

	margin: 25px 24px 24px 24px;
	display: flex;
	float: left;
}

#blockPhotoInfo2 {
	transition: .2s;

	display: flex;
}

#hr {
	transition: .2s;

	display: none;
}


@media (max-width: 1130px) {
	#main {
		width: 96.9%;
	}
	#blockAgent {
		flex-direction: column;
		display: flex;
		margin-top: 24px;
		margin-left: 0%;
	}
}

@media (max-width: 830px) {
	#blockPhotoInfo {
		margin-bottom: 0px;
		justify-content: center;
	}
	#main {
		height: fit-content;
		display: flex;
		flex-direction: column;
	}
	#blockAgentMain {
		justify-content: center;
		margin: 0px;
		margin-bottom: 24px;
	}
	#info {
		text-align: center;
		margin: 8px 0px 0px 32px;
	}
	#photoNetJobForce {
		margin: 0px;
	}
	#pageFranchise {
		justify-content: center;
	}
	#hr {
		margin: 0px;
		margin-left: 5%;
		margin-top: 24px;
		display: block;
		height: 1px;
		width: 90%;
		border: 0px;
		background-color: rgba(0, 0, 0, 0.2);
	}
	#btnRequestPhinplan {
		width: 295px;
	}
	#blockAgent {
		align-items: center;
	}
}

@media (max-width: 510px) {
	#blockPhotoInfo2 {
		flex-direction: column;
	}
	#photoNetJobForce {
		justify-content: center;
	}
	#info {
		text-align: center;
		margin: 8px 0px 0px 0px;
	}
}

</style>