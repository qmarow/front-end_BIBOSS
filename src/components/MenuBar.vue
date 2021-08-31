<template>
	<div>
			<input class="inputSearch" type='text' placeholder="Поиск" v-model="inputTxt" />
			<hr class="hrAfterInput">
			<ul class="list">
				<li>
					<img src="./../images/iconPeople.svg">
					<span>Сообщества</span>
				</li>
				<li>
					<img src="./../images/iconKN.svg">
					<span>Коммерческая недвижимоть</span>
				</li>
				<li>
					<img src="./../images/iconFD.svg">
					<span>Франшизы</span>
				</li>
				<li>
					<img src="./../images/iconGB.svg">
					<span>Готовый бизнес</span>
				</li>
				<li>
					<img src="./../images/iconOpt.svg">
					<span>Товары и услуги</span>
				</li>
				<li>
					<img src="./../images/iconSupplier.svg">
					<span>Поставщики</span>
				</li>
				<li>
					<img src="./../images/iconInvest.svg">
					<span>Инвестиции</span>
				</li>
				<li>
					<img src="./../images/iconIdea.svg">
					<span>Бизнес-идеи</span>
				</li>
				<li>
					<img src="./../images/iconBPlan.svg">
					<span>Бизнес-планы</span>
				</li>
			</ul>
	</div>
</template>


<script>
export default {
	props: {},
	data() {
		return {
			inputTxt: '',
		}
	},
	watch: {
	},
	components: {}
}
</script>


<style scoped>

.inputSearch {
	font-family: Arial;
	font-style: normal;
	font-weight: normal;
	font-size: 16px;
	line-height: 24px;
	color: rgba(0, 0, 0, 0.52);

	margin-left: 6px;
	margin-top: 6px;
	width: 72.5%;
	min-width: 120px;
	height: 40px;

	border: 1px solid rgba(0, 0, 0, 0.2);
	border-radius: 8px;

	padding-left: 44px;
	padding-right: 23px;
	
	background-image: url('./../images/iconSearch.svg');
	background-repeat: no-repeat;
	background-position-x: 12px;
	background-position-y: 8px;
	outline: none;
}.inputSearch:focus {
	border: 1px solid rgba(0, 0, 0, 0.2);
}.inputSearch:hover {
	box-shadow: 1px 5px 15px rgba(199, 199, 199, 0.336);
}

.hrAfterInput {
	width: 94%;
	margin: 8px;
	height: 1px;
	background-color: rgba(0, 0, 0, 0.2);
	border: 0px
}

.list {
	display: block;
	list-style-type: none;
  padding-left: 0;
	margin-left: 6px;
	margin-top: 6px;
	width: 95%;
}

li {
	display: flex;
	height: 40px;
	border: 1px solid rgba(129, 46, 46, 0);
	overflow: hidden;
	transition: 0.1s;
} li:hover {
	transform: translateX(10px);
}

img {
	margin-top: 10px;
	margin-left: 12px;
	width: 24px;
	height: 24px;
}

span {
	height: 24px;
	margin-top: 10px;
	margin-left: 8px;

	font-family: Arial;
	font-style: normal;
	font-weight: normal;
	font-size: 16px;
	line-height: 24px;
}

</style>