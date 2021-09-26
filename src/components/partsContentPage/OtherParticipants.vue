<template>
	<div id="main">
		<div id="title">Другие участники конкурса</div>
		<div id="blockOtherParticipans">
			<VideoOtherParticipans class="otherParticipant"
				ID="1"
				title="Borodach"
				text="Мужские парикмахерские"
				pathToFirstFrame="img-with-sheet.jpg"
				pathToVideo="FranchiseVideo.mp4"
				/>
			<VideoOtherParticipans class="otherParticipant"
				ID="2"
				title="Персональное решение"
				text="Сеть услуг рабочей силы"
				pathToFirstFrame="img-creative-guy.jpg"
				pathToVideo="FranchiseVideo.mp4"
				/>
			<VideoOtherParticipans class="otherParticipant"
				ID="3"
				title="TOY.RU"
				text="Магазин детских игрушек"
				pathToFirstFrame="img-table.jpg"
				pathToVideo="FranchiseVideo.mp4"
				/>
		</div>
		<button>Все участники конкурса</button>
	</div>
</template>


<script>
import VideoOtherParticipans from './auxiliaryElements/VideoOtherParticipans.vue'

export default {
	props: {},
	data() {
		return {}
	},
	components: {
		VideoOtherParticipans: VideoOtherParticipans,
	}
}
</script>


<style scoped>
#main {
	padding-bottom: 40px;
	margin-top: 40px;
	width: 1120px;
	font-family: Arial;
	font-style: normal;
}

#title {
	color: #000;
	opacity: 1;
	/* background-color: rgb(102, 93, 161); */
	font-weight: bold;
	font-size: 32px;
	line-height: 40px;
}

#blockOtherParticipans {
	padding: 0px;
	overflow: auto;
	display: flex;
	flex-direction: row;
}

.otherParticipant {
	margin-left: 32px;
}

.otherParticipant:first-child {
	margin: 0px;
}

button {
	margin-top: 32px;
	font-weight: bold;
	font-size: 16px;
	line-height: 24px;
	width: 240px;
	height: 50px;
	border: 1px solid rgba(0, 0, 0, 0.2);
	box-sizing: border-box;
	border-radius: 6px;
	background-color: #fff;
	color: #000000;
	transition: .2s;
} button:hover {
	color: #fff;
	background-color: rgba(0, 0, 0, 0.2);
}

p {
	font-size: 0px;
	line-height: 100px;
}

::-webkit-scrollbar {
	display: none;
}

@media (max-width: 1130px) {
	#main {
		width: 100%;
	}
	#title {
		margin-left: 2%;
	}
	button {
		margin-left: 2%;
	}
	.otherParticipant:first-child {
		margin-left: 2%;
	}
}

@media (max-width: 830px) {
	#main {
		margin-top: 8px;
	}
	#title {
		font-size: 24px;
		line-height: 32px;
	}
}

</style>