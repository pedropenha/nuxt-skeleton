<template>
	<div>ola mundo</div>
</template>

<script>

import { fas } from '@fortawesome/free-solid-svg-icons'

export default{
	props:{
		borderColor:{
			type: String,
			required: true
		},
		bgColor:{
			type: String,
			required: true
		},
		legendText:{
			type: String,
			required: true
		},
		peopleGroup:{
			type: String,
			required: true
		},
	},
	computed: {
		fas () {
				return fas
		},
	},
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

</style>