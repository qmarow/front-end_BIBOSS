<template>
	<div id="main">
			<div id="title-logo">
					<div id="logo-block">
						<img id="icon-logo" src="./../images/iconBiBOSS.svg" />
						<div id="text-logo">БИБОСС</div>
					</div>
					<div id="controll">
							<img id="img-svg" src='./../images/iconFlesh.svg'/>
							<div id="txt-controll">Управление</div>
					</div>
			</div>
			<div>
				<Section />
			</div>
	</div>
</template>


<script>
import "./componentsBasement/style-column.css"
import Section from './componentsBasement/Section.vue'

export default {
	props: {},
	data() {
		return {}
	},
	components: {
		Section: Section,
	}
}
</script>


<style scoped>

#main {
		padding-top: 40px;
		padding-left: 48px;
		width: 100%;
		background-color: rgba(51, 51, 51, 1);
		font-family: Arial;
		font-style: normal;
}

#title-logo {
		display: flex;
}

#logo-block {
		display: flex;
		color: #fff;
}

#text-logo {
		font-weight: bold;
		font-size: 24px;
		line-height: 24px;
		margin-left: 8px;
}

#icon-logo {
		width: 24px;
		height: 24px;
}

#controll {
		display: flex;
		margin-left: 24px;
}

#txt-controll {
		font-weight: normal;
		font-size: 14px;
		line-height: 20px;
		color: #FFFFFF;
		opacity: 0.4;
		margin-left: 8px;
}

#img-svg  {
		width: 24px;
		height: 24px;
}

</style>