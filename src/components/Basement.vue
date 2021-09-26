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
		<div id="columnsBasement">
			<div class="column">
				<Section />
			</div>
			<div class="column">
				<Project />
			</div>
			<div class="column">
				<BEBOSS />
			</div>
			<div class='column'>
				<SocialNetwork />
			</div>
		</div>
		<hr />
		<div id='basement'>
			<div id="BlockCountry">
				<span id="txtOtherCountry">ДРУГИЕ СТРАНЫ</span>
				<div class="country">
					<div class='YkrainianFlag'>
						<div class="imposition">
						</div>
					</div>
					<span class="nameCountry">Украина</span>
				</div>
				<div class="country">
					<div class='KazakhstanFlag'>
						<div class="imposition">
						</div>
					</div>
					<span class="nameCountry">Казахстан</span>
				</div>
				<div class="country">
					<div class='BelarusFlag'>
						<div class="imposition">
						</div>
					</div>
					<span class="nameCountry">Казахстан</span>
				</div>		
			</div>
			<div id="blockLink">
				<span class="nameCountry">© БИБОСС 2006-2018</span>
				<img id='imglink' src="./../images/l2t1bt-N9EE.jpg"/>
			</div>
		</div>
	</div>
</template>


<script>
import "./componentsBasement/style-column.css"
import Section from './componentsBasement/Section.vue'
import Project from './componentsBasement/Project.vue'
import BEBOSS from './componentsBasement/BEBOSS.vue'
import SocialNetwork from './componentsBasement/SocialNetwork.vue'
export default {
	props: {},
	data() {
		return {}
	},
	components: {
		Section: Section,
		Project: Project,
		BEBOSS: BEBOSS,
		SocialNetwork: SocialNetwork,
	}
}
</script>


<style scoped>

#main {
	box-sizing: border-box;
	padding: 40px 48px 16px;
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

#columnsBasement {
	display: flex;
}

.column {
	margin-left: 63px;
}.column:first-child {
	margin-left: 0px;
}

hr {
	margin-top: 24px;
	background: rgba(0, 0, 0, 0.2);
	border: 0px;
	border-radius: 2px;
	height: 2px;
	width: 100%;
}

#basement {
	height: 31px;
	align-items: center;
}

#BlockCountry {
	float: left;
	display: flex;
	align-items: center;
	height: 100%;
}

#blockLink {
	display: flex;
	align-items: center;
	justify-content: right;
}

#txtOtherCountry {
	font-weight: bold;
	font-size: 14px;
	line-height: 20px;
	color: #FFFFFF;
	opacity: 0.6;
}

.country {
	margin-left: 24px;
	display: flex;
	align-items: center;
}

.nameCountry {
	margin-left: 8px;
	font-weight: normal;
	font-size: 14px;
	line-height: 20px;
	color: #FFFFFF;
	opacity: 0.4;
}

.imposition{
	background-color: rgba(43, 43, 43, 0.507);
	width: 100%;
	height: 100%;
	border-radius: 4px;
}

.YkrainianFlag {
	background-image: url(./../images/YkrainianFlag.jpg);
	background-repeat: no-repeat;
	background-size: 100%;
	width: 48px;
	height: 24px;
		border-radius: 4px;
}

.KazakhstanFlag {
	background-image: url(./../images/KazakhstanFlag.jpg);
	background-repeat: no-repeat;
	background-size: 100%;
	width: 48px;
	height: 24px;
	border-radius: 4px;
}

.BelarusFlag {
	background-image: url(./../images/BelarusFlag.jpg);
	background-repeat: no-repeat;
	background-size: 100%;
	width: 48px;
	height: 24px;
	border-radius: 4px;
}

#imglink {
	width: 88px;
	height: 31px;
	margin-left: 24px;
}

</style>