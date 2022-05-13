<template>
	<nav class="menu-opcoes">
		<ul>
			<li>
				<button class="button-icone" title="Ajuda">
					<fa :icon="fas.faCircleQuestion" class="btn-ajuda"/>
				</button>
			</li>
			<li>
				<button class="button-icone" title="Contraste">
					<fa :icon="fas.faCircleHalfStroke" class="btn-contraste"/>
				</button>
			</li>
			<li>
				<button class="button-icone" title="Configuração de tamanho de fonte">
					<fa :icon="fas.faA" class="btn-letra"/>
				</button>
			</li>
			<li>
				<button class="button-icone" title="Configurações">
					<fa :icon="fas.faGear" class="btn-settings"/>
				</button>
			</li>
		</ul>
	</nav>
</template>

<script>
import { fas } from '@fortawesome/free-solid-svg-icons'

export default {
	computed: {
		fas () {
				return fas
		},
	},
}
</script>

<style scoped>
.menu-opcoes{
  border-bottom: 1px solid #5f9ea0;
  margin-top: 5px;
	background-color: transparent;
}

ul{
  list-style: none;
  display: flex;
  justify-content: center;
}

.button-icone{
	background-color: transparent;
	padding: 10px;
	border: 2px solid transparent;
	border-radius: 5px;
	margin: 5px;
	transition: all .5s ease;
	cursor: pointer;
}

.button-icone:hover{
	box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}

.btn-ajuda{
    color: #e04a3a;
	font-size: 24px;
}

.btn-contraste{
    color: #3293d4;
	font-size: 24px;
}

.btn-contraste{
    color: #3293d4;
	font-size: 24px;
}

.btn-letra{
	color: black;
	font-size: 24px;
}
.btn-settings{
	color: #202020;
	font-size: 24px;
}
</style>