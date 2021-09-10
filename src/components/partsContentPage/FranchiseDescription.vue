<template>
	<div>
		<div>
				<TitleWithHR>Описание франшизы</TitleWithHR>
		</div>
		<div>
			<p>ЧЕМ ТЫ БУДЕШЬ ЗАНИМАТЬСЯ? И КАК БУДЕШЬ ЗАРАБАТЫВАТЬ НА УСЛУГАХ РАБОЧЕЙ СИЛЫ?</p>
			<p>Ты будешь предоставлять рабочую силу на склады, фабрики, заводы, производства со сдельной и почасовой оплатой.</p>
			<p>Кто будет работать у тебя?</p>
				<ul>
					<li>Рабочие, ищущие дополнительный заработок</li>
					<li>Временно безработные люди</li>
				</ul>
		</div>
		<div>
			<OpeningTag>Страница франшизы</OpeningTag>
		</div>
	</div>
</template>


<script>
import TitleWithHR from './auxiliaryElements/TitleWithHR.vue'
import OpeningTag from './auxiliaryElements/OpeningTag.vue'

export default {
	props: {},
	data() {
		return {}
},
	components: {
			TitleWithHR: TitleWithHR,
			OpeningTag: OpeningTag,
	}
}
</script>


<style scoped>
</style>