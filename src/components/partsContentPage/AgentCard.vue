<template>
	<div id="main">
		<div>
			<BlockAgent />
		</div>
		<!-- <div :style="{'display': 'flex'}">
			<div id="blockInput">
				<input id="name" type='text' placeholder="Ваше имя"/>
				<input id="mail" type='text' placeholder="E-mail"/>
				<input id="phone" type='text' placeholder="Номер телефона"/>
				<textarea>Здравствуйте. Заинтересовало Ваше предложение, вышлите подробности на почту.</textarea>
				<div id="captcha">
					<input id="checkBox" type="checkbox">
					<span :style="{'margin-left': '8px'}">Я не робот</span>
					<span id="txtChSec" >Проверка безопасности</span>
				</div>
				<button id="btnSendMess">Отправить сообщение</button>
			</div>
			<div id="blockQuestions">
				<div :style="{'font-weight': 'bold', 'line-height': '24px'}"
					>Что можно обсудитьс представителем:
				</div>
				<div class="question">
					<img class="imgOkey" src="./../../images/iconOkey.svg" />
					Узнать есть ли возможность открытия в вашем городе
				</div>
				<div class="question">
					<img class="imgOkey" src="./../../images/iconOkey.svg" />
					Попросить контакты уже действующих франчайзи
				</div>
				<div class="question">
					<img class="imgOkey" src="./../../images/iconOkey.svg" />
					Получить шаблоны договоров для ознакомления
				</div>
				<div class="question">
					<img class="imgOkey" src="./../../images/iconOkey.svg" />
					Ознакомиться с финансовым планом и этапами запуска бизнеса
				</div>
				<div class="question">
					<img class="imgOkey" src="./../../images/iconOkey.svg" />
					Узнать какие гарантии может дать франшиза
				</div>
				<div class="question">
					<img class="imgOkey" src="./../../images/iconOkey.svg" />
					Обсудить возможность скидки
				</div>
			</div>
		</div> -->
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
	width: 700px;
	padding: 24px 0px 24px 24px;
	border-radius: 16px;
	background-color: #5077c4;
	font-family: Arial;
	font-style: normal;
}

#blockInput {
	margin-top: 8px;
	display: flex;
	flex-direction: column;
}

input, textarea {
	margin-top: 8px;
	width: 378px;
	height: 42px;
	background: #FFFFFF;
	border: 1px solid rgba(0, 0, 0, 0.2);
	box-sizing: border-box;
	border-radius: 6px;
	padding-left: 44px;
	font-weight: normal;
	font-size: 16px;
	line-height: 24px;
	outline: none;
}

textarea {
	line-height: 24px;
	font-size: 14px;
	padding-left: 9px;
	padding-top: 8px;
	height: 86px;
}

#name {
	background-image: url('./../../images/iconOnePeople.svg');
	background-repeat: no-repeat;
	background-position-x: 15px;
	background-position-y: 11px;
}

#mail {
	background-image: url('./../../images/iconMail.svg');
	background-repeat: no-repeat;
	background-position-x: 13px;
	background-position-y: 12px;
}

#phone {
	background-image: url('./../../images/iconPhone.svg');
	background-repeat: no-repeat;
	background-position-x: 17px;
	background-position-y: 10px;
}

#captcha {
	background: #ECEEF2;
	border: 1px solid rgba(0, 0, 0, 0.2);
	box-sizing: border-box;
	border-radius: 6px;
	width: 378px;
	height: 80px;
	display: flex;
	margin-top: 8px;
	align-items: center;
	padding-left: 16px;
	padding-right: 16px;
}

#checkBox {
	/* margin-top: 24px; */
	margin-left: 16px;
	width: 32px;
	height: 32px;
	margin: 0px;
	display: inline-block;
}

#txtChSec {
	display: flex;
	font-size: 14px;
	line-height: 20px;
	text-align: right;
	color: rgba(0, 0, 0, 0.52);
	width: 40px;
	margin-left: 133px;
	margin-left: 38.5%;
}

#btnSendMess{
	margin-top: 8px;
	background: #0D870D;
	border-radius: 6px;
	width: 378px;
	height: 50px;
	color: #FFFFFF;
	border: 0px solid #fff0;
	font-weight: bold;
	font-size: 16px;
	line-height: 24px;
	transition: 0.2s;
} #btnSendMess:hover {
	transform: translateY(-0.5px);
	background: #fff;
	color: #0D870D;
	border: 2px solid #0D870D;
	width: 378px;
	height: 50px;
}

#blockQuestions {
	width: 370px;
	margin-top: 16px;
	margin-left: 32px;
	/* background-color: azure; */
}

.question {
	margin-top: 16px;
	line-height: 24px;
}

.imgOkey {
	margin-right: 11px;
	width: 18px;
	height: 13px;
}

</style>