<template>
	<div id="main">
		<div>
			<BlockAgent />
		</div>
		<div id='blockData'>
			<div id="blockInput">
				<input id="name" type='text' placeholder="Ваше имя"/>
				<input id="mail" type='text' placeholder="E-mail"/>
				<input id="phone" type='text' placeholder="Номер телефона"/>
				<textarea>Здравствуйте. Заинтересовало Ваше предложение, вышлите подробности на почту.</textarea>
				<div id="captcha">
					<div id="divCheckBoxAndTxt">
						<input id="checkBox" type="checkbox">
						<span :style="{'margin-left': '8px'}">Я не робот</span>
					</div>
					<div id="divTxtChSec">
						<span id="txtChSec" >Проверка безопасности</span>
					</div>
				</div>
				<button id="btnSendMess">Отправить сообщение</button>
				<div id="blockSecTxtIcon">
					<img src="./../../images/iconProtection.svg" >
					<span id="secTxt">Ваши данные в полной безопасности. Они видны только автору объявления.</span>
				</div>
				<hr id='hr'>
			</div>
			<div id="blockQuestions">
				<div id="titleQuestions">
					Что можно обсудить с представителем:
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
	box-sizing: border-box;
	width: 832px;
	padding: 24px;
	border-radius: 16px;
	background-color: rgba(236, 238, 242, 1);
	font-family: Arial;
	font-style: normal;
}

#blockData {
	display: flex;
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

	margin-top: 8px;
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

#divCheckBoxAndTxt {
	margin-top: 24px;
	display: flex;
	align-items: center;
	float: left;
}

#txtChSec {
	display: flex;
	text-align: right;
	color: rgba(0, 0, 0, 0.52);
	font-size: 14px;
	line-height: 20px;
	width: 90px;
	/* margin-left: 38.5%; */
}

#divTxtChSec {
	margin-top: 21px;
	display: flex;
	justify-content: right;
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

#blockSecTxtIcon {
	width: 378px;
	margin-top: 16px;
	display: flex;
	font-size: 14px;
	line-height: 20px;
	color: rgba(0, 0, 0, 0.4);
}

#secTxt {
	margin-left: 16px;
}

#blockQuestions {
	width: 370px;
	margin-top: 16px;
	margin-left: 32px;
	/* background-color: azure; */
}

#titleQuestions {
	font-weight: bold;
	line-height: 24px;
}

.question {
	margin-top: 16px;
	line-height: 24px;
	display: flex;
}

.imgOkey {
	margin-right: 11px;
	width: 18px;
	height: 13px;
}

#hr {
	background: rgba(0, 0, 0, 0.2);
	border: 0px;
	height: 1px;
	width: 100%;
	margin-top: 24px;
	display: none;
}

@media (max-width: 1130px) {
	#blockData {
		display: flex;
		/* flex-direction: column; */
		/* align-i.tems: center; */
		justify-content: space-around;
	}
	#blockInput {
		display: flex;

		width: fit-content;
	}
	#blockQuestions {
		margin-left: 0px;
		width: fit-content;
	}
}

@media (max-width: 1035px) {
	#blockQuestions {
		margin-left: 16px;
		width: fit-content;
	}
}

@media (max-width: 830px) {
	#blockInput {
		width: 70%;
	}
	#blockQuestions {

		width: 70%;
	}
	input, textarea {
		width: 100%;
	}
	#captcha {
		width: 100%;
	}
	#btnSendMess {
		width: 100%;
	} #btnSendMess:hover {
		width: 100%;
	}

	#blockSecTxtIcon {
		width: 100%;
	}
}

@media (max-width: 625px) {
	#blockData {
		flex-direction: column;
	}
	#blockInput {
		width: 100%;
		display: flex;
		align-items: center;
	}
	#blockQuestions {
		display: flex;
		flex-direction: column;
		width: 100%;
		margin: 0px;
		margin-top: 24px;
		box-sizing: border-box;
		align-items: right;
		/* display: flex; */
		/* align-items: center; */
	}
	input, textarea {
		width: 100%;
	}
	#captcha {
		width: 100%;
	}
	#hr {
		display: block;
	}

	#titleQuestions {
		font-weight: bold;
		line-height: 24px;
		text-align: center;
	}
}

</style>