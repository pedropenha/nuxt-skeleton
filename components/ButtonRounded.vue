<template>
	<button :style="'background-color:'+ bgColor +';color:'+ color +';border-color:'+ borderColor +';border-radius:'+ borderRadius +';'" class="btn">
		<b>{{labelButton}}</b>
	</button>
</template>

<script>
export default{
	props: {
		labelButton:{
			type: String,
			required: true
		},
		bgColor:{
			type: String,
			required: true
		},
		color:{
			type: String,
			required: true
		},
		borderColor:{
			type: String,
			required: true
		},
		borderRadius:{
			type: String,
			required: false,
			default: "100px"
		}
	},
}
</script>

<style scoped>

.btn{
	width: 100%;
	cursor: pointer;
	padding: 5px 15px;
	border-style: solid;
	border-width: 2px;
	transition: all 1s ease;
}

.btn:hover{
	box-shadow: rgba(0, 0, 0, 0.8) 0px 5px 15px;
}

</style>