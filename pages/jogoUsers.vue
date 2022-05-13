<template>

	<section id="main">
			<div class="container">
					<ImgLogo :maxWidth="'300px'"/>
					<div class="bloco mb-2">
            <AccessibilityList/>
            <ListUsers legendText="Pessoas cadastradas" peopleGroup="Grupo de no máximo 3 pessoas" class="mt-1" levelMessage="Escolher o nível" buttonMessage="Jogar"/>
            <fieldset class="cadastros">
              <legend>
                <b>Cadastrar pessoas</b>
              </legend>
              <div class="form-flex-group">
                <label>Novo usuário</label>
                <div class="flex-largura-restante">
                  <input placeholder="Nome ou código do aluno" required="required" type="text" autocomplete="off"/>
                </div>
              </div>
              <div style="width: 40%;background-color: #f6f7fd;" class="mt-1">
			          <ButtonRounded labelButton="Adicionar" bgColor="#1c864a" color="white" borderColor="#1c864a"/>
		          </div>
            </fieldset>
          </div>
			</div>
	</section>

</template>

<script>
import ImgLogo from "../components/imgLogo.vue";
import AccessibilityList from "~/components/AccessibilityList.vue";
import ListUsers from "~/components/ListUsers.vue";
import ButtonRounded from "~/components/ButtonRounded.vue";
export default{
  components:{ ImgLogo, AccessibilityList, ListUsers, ButtonRounded }
}
</script>

<style scoped>

*{
  margin: 0;
  padding: 0;
  background-color: #cbdee9;
}

.bloco{
  background-color: #f6f7fd;
  border-radius: 15px;
  padding: 15px;
  box-shadow: 0 0.4rem 0.8rem -0.1rem rgb(0 32 128 / 10%), 0 0 0 1px #f0f2f7;
  border: 3px solid #5f9ea0;
  max-width: 95%;
  margin: 0 auto;
  width: 35%;
}

.cadastros{
  padding: 15px;
  border: 1px solid #dbd1d1;
  border-radius: 12px;
  margin-bottom: 15px;
  background-color: #f6f7fd !important;
}

.cadastros > legend > b{
  background-color: #f6f7fd;
}

.form-flex-group{
  display: flex;
  padding-bottom: 5px;
  margin-bottom: 5px;
  background-color: #f6f7fd !important;
}

.form-flex-group > label{
  margin-right: 15px;
  background-color: #f6f7fd !important;
}

.flex-largura-restante{
  flex-grow: 1;
  background-color: #f6f7fd !important;
}

.flex-largura-restante > input{
  border-radius: 100px;
  padding: 5px 15px;
  border-style: solid;
  border-color: #e2e2e2;
  background-color: #fff !important;
  width: 90%;
}

@media(min-width: 320px) and (max-width: 1100px){
  .bloco{
    width: 100%;
  }
}
@media(min-width: 1101px) and (max-width: 1600px){
  .bloco{
    width: 40%;
  }
}
</style>