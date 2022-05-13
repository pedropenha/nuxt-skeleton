<template>
	<fieldset class="listaUsuarios" :style="'border:2px solid '+ borderColor +';background-color:'+ bgColor +';'">
		<legend>
			<b>{{legendText}}</b>
		</legend>
		<p class="subtitulo">{{peopleGroup}}</p>
		<ul class="listagem">
			<li>
				<input type="checkbox" class="listagem-input">
				<label class="listagem-label">Evandro</label>
				<button title="Excluir usuario" class="listagem-button"><fa :icon="fas.faTrashCan" class="btn-ajuda"/></button>
			</li>
			<li>
				<input type="checkbox" class="listagem-input">
				<label class="listagem-label">Evandro</label>
				<button title="Excluir usuario" class="listagem-button"><fa :icon="fas.faTrashCan" class="btn-ajuda"/></button>
			</li>
			<li>
				<input type="checkbox" class="listagem-input">
				<label class="listagem-label">Evandro</label>
				<button title="Excluir usuario" class="listagem-button"><fa :icon="fas.faTrashCan" class="btn-ajuda"/></button>
			</li>
		</ul>
		<div class="gameNivel">
			<p class="level">{{levelMessage}}</p>
			<div class="escolher-fase">
				<div class="first-element">
					<input type="radio" checked="checked" class="is-sr-only">
					<label>Nível 01</label>
				</div>
				<div>
					<input type="radio" class="is-sr-only">
					<label>Nível 02</label>
				</div>
				<div class="last-element">
					<input type="radio" class="is-sr-only">
					<label>Nível 03</label>
				</div>
			</div>
			<div class="escolher-fase mt-1">
				<div class="first-element">
					<input type="radio" class="is-sr-only">
					<label>Nível 04</label>
				</div>
				<div>
					<input type="radio" class="is-sr-only">
					<label>Nível 05</label>
				</div>
				<div>
					<input type="radio" class="is-sr-only">
					<label>Nível 06</label>
				</div>
				<div class="last-element">
					<input type="radio" class="is-sr-only">
					<label>Nível 07</label>
				</div>
			</div>
		</div>
		<hr/>
		<div style="width: 40%;" class="mt-1">
			<ButtonRounded :labelButton="buttonMessage" bgColor="#1c864a" color="white" borderColor="#1c864a"/>
		</div>
	</fieldset>
</template>

<script>

import { fas } from '@fortawesome/free-solid-svg-icons'
import ButtonRounded from './ButtonRounded.vue';

export default{
    props: {
        borderColor: {
            type: String,
            required: true
        },
        bgColor: {
            type: String,
            required: true
        },
        legendText: {
            type: String,
            required: true
        },
        peopleGroup: {
            type: String,
            required: true
        },
        levelMessage: {
            type: String,
            required: true
        },
				buttonMessage: {
					type: String,
					required: true
				}
    },
    computed: {
        fas() {
            return fas;
        },
    },
    components: { ButtonRounded }
}
</script>
<style scoped>

.listaUsuarios{
	border-radius: 12px;
	margin-bottom: 15px;
	background-color: white;
	padding: 15px;
}

.listagem{
	list-style: none;
	width: 100%;
	max-height: 300px;
	overflow-x: hidden;
	margin-bottom: 15px;
}

.listagem > li{
	width: 100%;
	padding: 10px;
	padding-left: 5px;
	text-decoration: none;
	display: block;
	color: #47b382;
	border-bottom: 1px dotted #e2e2e2;
	font-weight: bold;
}

.itemList{
	display: flex;
	background-color: white;
	align-items: center;
	justify-content: space-between;
	padding: 15px;
	transition: all .5s ease;
}

.itemList:hover{
	box-shadow: rgba(0, 0, 0, 0.5) 0px 5px 15px 0px;
}

.itemList > label{
	font-size: 18px;
}

.border-top-rounded{
	border-top-left-radius: 15px;
	border-top-right-radius: 15px;
}

.border-bottom-rounded{
	border-bottom-left-radius: 15px;
	border-bottom-right-radius: 15px;
}

.listagem-input{
	border-radius: 100px;
	padding: 5px 15px;
	border-style: solid;
	border-color: #e2e2e2;
}

.listagem-button{
	float: right;
	padding: 2px 10px;
	color: rgb(59, 59, 59);
	background-color: transparent;
	border-radius: 2px;
	border: 1px dotted #ccc;
	margin-right: 10px;
	transition: all .5s ease;
	cursor: pointer;
}

.listagem-button:hover{
	box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}

.gameNivel{
	padding: 7px 0px 15px 0;
	margin-bottom: 15px;
	margin-bottom: 1px solid #e2e2e2;
}

.level{
	margin: 5px 0;
}

.escolher-fase{
	width: 100%;
	display: flex;
	justify-self: center;
	text-align: center;
	border: 1px solid #217ab6;
	border-radius: 7px;
}

.escolher-fase > div{
	width: 50%;
}

.is-sr-only{
	border: none!important;
	clip: rect(0,0,0,0)!important;
	height: 0.01em!important;
	overflow: hidden!important;
	padding: 0!important;
	position: absolute!important;
	white-space: nowrap!important;
	width: 0.01em!important;
}

input[type="radio" i]{
	background-color: initial;
	cursor: default;
	appearance: auto;
	box-sizing: border-box;
	margin: 3px 3px 0px 5px;
	padding: initial;
	border: initial;
}

.escolher-fase > div input:checked + label{
	background-color: #3293d4;
	color: white;
}

.escolher-fase > div input + label{
	cursor: pointer;
}

.first-element{
	border-top-left-radius: 7px;
	border-bottom-left-radius: 7px;
}

.last-element{
	border-top-right-radius: 7px;
	border-bottom-right-radius: 7px;
}

.escolher-fase > div{
	transition: all .5s ease;
}

.escolher-fase > div:hover{
	box-shadow: rgba(0, 0, 0, 0.8) 0px 5px 15px;
}

.escolher-fase > div label{
	padding: 5px;
	display: block;
}

input{
	cursor: pointer;
}

.btnJogar{

}
</style>