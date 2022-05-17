<template>
	<section id="main">
		<div class="mascara-cenario"></div>
		<div class="infos">
			<div class="info-nivel">
				<div class="titulo-game">
					<h4>Game Trek Music</h4>
					<h1 class="nivel">Nível 1</h1>
				</div>
			</div>
			<div class="actions-button">
				<div class="actions-button-group mt-1">
					<button class="btn btn-desempenho">
						<span>Tiago</span>
						<span> - 0 pontos</span>
						<br/>
						<span>Ver desempenho</span>
					</button>
					<button class="btn btn-ajuda">
						<span>Ajuda</span>
					</button>
					<button class="btn btn-ajuda">
						<span>Configurações</span>
					</button>
					<button class="btn btn-fechar-cenario">
						<div>
							<fa :icon="fas.faXmark"/>
						</div>
					</button>
				</div>
			</div>
		</div>
		<main class="conteudo-cenario">
			<a class="fases">
				<img src="../static/img/fase01.svg" class="ilustracao-fase height145px"/>
			</a>
			<div class="bandeira">
				<img class="bandeira-img" src="../static/img/bandeira.svg"/>
			</div>
			<div class="trilha"></div>
			<a class="fases">
				<img src="../static/img/fase01.svg" class="ilustracao-fase height145px"/>
			</a>
			<div class="bandeira">
				<img class="bandeira-img" src="../static/img/bandeira.svg"/>
			</div>
			<div class="trilha"></div>
			<a class="fases">
				<img src="../static/img/fase01.svg" class="ilustracao-fase height145px"/>
			</a>
			<div class="bandeira">
				<img class="bandeira-img" src="../static/img/bandeira.svg"/>
			</div>
			<div class="trilha"></div>
		</main>
		<div id="conjuntoSetas" role="group" aria-label="Links para movimentação do cenário">
			<a id="setaEsq" @Click="scrollEsq" title="Visualizar mais itens à esquerda" class="rotacionar180"></a>
			<a id="setaDir" @Click="scrollDir" title="Visualizar mais itens à direita"></a>
		</div>
	</section>
</template>

<script>
import { fas } from '@fortawesome/free-solid-svg-icons'
export default{
	computed:{
		fas() {
			return fas;
		},
	},
	methods:{
		scrollEsq(){
			const mascara = document.getElementsByClassName('mascara')[0];
			this.scrollTo(mascara, mascara.scrollLeft - 500, 200);
		},
		scrollDir(){
			const mascara = document.getElementsByClassName('mascara')[0];
			this.scrollTo(mascara, mascara.scrollLeft + 500, 200);
		}
	}
}
</script>

<style scoped>

#main{
	width: 100vw;
	height: 100vh;
	overflow: hidden;
	background-image: url('../static/img/cenario.png');
	transform-origin: top left;
	overflow: hidden;
	background-repeat: no-repeat;
	background-size: auto 100%;
	position: relative;
}

.mascara-cenario{
	width: 100%;
	position: absolute;
	top: 0;
	left: 0;
	bottom: 0;
	overflow-y: hidden;
}

.infos{
	display: flex;
	justify-content: space-between;
	height: auto;
	width: 100%;
}

.conteudo-cenario{
	position: absolute;	
	bottom: 280px;
	display: flex;
	padding-left: 130px;
	height: 165px;
	transform: scale(2);
	margin-left: 20%;
}

.conteudo-cenario > *{
	align-self: flex-end;
}

.info-nivel{
	width: 210px;
	height: 160px;
	border-bottom-right-radius: 100%;
	background-color: slateblue;
	display: flex;
	flex-wrap: wrap;	
	color: white;
	border-right: 2px solid white;
	border-bottom: 2px solid white;
}

.fases{
	border: 2px solid transparent;
}

.ilustracao-fase{
	cursor: pointer;
	filter: drop-shadow(2px 0px 0 white) drop-shadow(0px 2px 0 white) drop-shadow(0px -2px 0 white) drop-shadow(-2px 0px 0 white);
}

.ilustracao-fase:hover{
	filter: drop-shadow(2px 0px 0 #ffcc00) drop-shadow(0px 2px 0 #ffcc00) drop-shadow(0px -2px 0 #ffcc00) drop-shadow(-2px 0px 0 #ffcc00);
}

.height145px{
	height: 145px;
}

.bandeira{
	z-index: 10;
	margin-right: -55px;
	margin-left: -41px;
	cursor: pointer;
}

.bandeira-img{
		max-height: 115px;
    left: 376px;
    top: 41px;
    width: 90px;
    margin-bottom: 5px;
}

.trilha{
	width: 190px;
	height: 11px;
	background-image: url('../static/img/trilha.svg');
	background-repeat: repeat-x;
	margin-bottom: 10px;
}

.nivel{
	font-size: 2rem !important;
}

.titulo-game{
	height: fit-content;
	padding: 5%;
}

.actions-button{
	width: 30%;
}

.btn-desempenho{
	border-radius: 5px;
	background-color: #FFC900;
	box-shadow: 0 0 1px #fef500, 0 0 0 4px #dcb000, 0 0 0 6px white, 0 0 0 8px #962a06;
}

.btn-desempenho:hover{
	transform: scale(1.1);
}

.btn-ajuda{
	border-radius: 5px;
	background-color: #91daf2;
	box-shadow: 0 0 0 1px #bce7f5, 0 0 0 4px #66cff2, 0 0 0 6px white, 0 0 0 8px #962a06;
}

.btn-ajuda > span{
	padding: 20px;
}

.btn-ajuda:hover{
	transform: scale(1.1);
}

.btn-fechar-cenario{
	width: 48px;
	height: 48px;
	background-color: #c0392b;
	color: white;
	border-radius: 50%;
}

.btn-fechar-cenario > div{
	width: 100%;
	height: 100%;
	display: flex;
	justify-content: center;
	align-items: center;
}

.btn-fechar-cenario:hover{
	transform: scale(1) rotate(90deg);
	border: 4px solid darkred !important;
	background-color: #a12517;
}

.fa-xmark{
	font-weight: 400 !important;
	font-size: 30px !important;
}

.btn{
	display: inline-block;
	font-weight: bold;
	padding: 5px;
	position: relative;
	transition: all .5s ease;
	cursor: pointer;
	border: 0;
}

.actions-button-group{
	width: 100%;
	height: auto;
	display: flex;
	align-items: flex-start;
	justify-content: space-around;
}

#conjuntoSetas{
	animation: fadeIn 0.2s linear;
	animation-delay: 10s;
	animation-fill-mode: forwards;
}

#conjuntoSetas a{
	height: 25%;
	width: 6%;
	background-color: rgba(0, 0, 0, 0.7);
	position: fixed;
	top: 50%;
	margin-top: -6.75%;
	transition: .1s;
	background-repeat: no-repeat;
	background-position: center;
	background-size: contain;
	background-image: url('../static/img/seta_cenario.svg');
	z-index: 100000;
	cursor: pointer;
}

#conjuntoSetas a:hover{
	width: 8%;
	background-color: rgba(0, 0, 0, 0.8);
}

#setaEsq{
	left: 0;
}

#setaDir{
	right: 0;
}

.rotacionar180{
	transform: rotate(180deg);
}

</style>