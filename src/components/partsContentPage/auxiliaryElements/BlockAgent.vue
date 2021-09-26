<template>
	<div :style="{'display': 'inline-block'}">
		<div id="agentInfo">
			<img id='imgAgent' src="./../../../images/photoAgent.svg" />
			<div id='txtInfo'>
				<p>Дмитрий Варфоломеев</p>
				<p>Представитель</p>
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

#imgAgent {
	height: 48px;
	width: 48px;
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

#blockAgent {
	margin-top: 24px;
	margin-left: 34%;
}

</style>