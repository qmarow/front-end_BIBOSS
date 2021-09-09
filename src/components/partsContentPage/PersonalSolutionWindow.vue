<template>
  <div id="main">
		<div id="photoNetJobForce">
			<img src="./../../images/photoNetJobForce.svg" />
		</div>
		<div id="info">
			<span id="personalSolution" >Персональное решение</span>
			<span id="investments" >Инвестиции 378 000 — 675 000 ₽</span>
			<div id="pageFranchise">Страница франшизы
				<img :style="{'margin-left': '8px'}" src="./../../images/iconMiniArrawRight.svg" />
			</div>
		</div>
		<div id="blockAgent">
			<div id="agentInfo">
				<img src="./../../images/photoAgent.svg" />
				<div id='txtInfo'>
					<p>Дмитрий Варфоломеев</p>
					<p>Представитель</p>
				</div>
			</div>
			<div>
				<button id="btnRequestPhinplan">Запросить финплан</button>
			</div>
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
	display: flex;
	width: 1120px;
	height: 162px;
	background: #FFFFFF;
	box-shadow: 0px 10px 40px rgba(0, 0, 0, 0.15);
	border-radius: 16px;
}

#photoNetJobForce {
	margin: 25px 24px 24px 24px;
}

#info {
	margin-top: 32px;
	font-family: Arial;
	font-style: normal;
}

#personalSolution {
	display: block;
	font-weight: bold;
	font-size: 24px;
	line-height: 32px;
}

#investments {
	display: block;
	margin-top: 8px;
	font-weight: normal;
	font-size: 16px;
	line-height: 24px;
}

#pageFranchise {
	display: flex;
	margin-top: 8px;
	font-weight: bold;
	font-size: 16px;
	line-height: 24px;
}

#agentInfo {

	display: flex;
	font-family: Arial;
	font-style: normal;
	font-weight: normal;
	font-size: 16px;
	line-height: 24px;
}

#txtInfo {
	margin-left: 8px;
	padding: 0px;
} #txtInfo p {
	padding: 0px;
	margin: 0px;
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
	margin-top: 24px;
	margin-left: 34%;
}

</style>