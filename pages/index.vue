<template>
  <section id="main">
    <div class="container">
      <ImgLogo :maxWidth="'200px'"/>
      <div class="forms">
        <InputLabel :id="'acessarCodigo'" :textoLabel="'Insira o código de acesso.'" :tipo="'text'" :name="'cod'" :textPlaceholder="'Código de acesso'"/>
        <ButtonGroup :labelButton="'Acessar'" :color="'success'" class="mt-2"/>
      </div>
    </div>
  </section>
</template>

<script>
import ImgLogo from '../components/imgLogo.vue';
import ButtonGroup from '~/components/ButtonGroup.vue';
import InputLabel from '~/components/InputLabel.vue';
export default {
  name: "IndexPage",
  components: { ButtonGroup, InputLabel, ImgLogo }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}

.forms{
  width: 50%;
}

@media(min-width: 320px) and (max-width: 1100px){
  .forms{
    width: 80%;
  }
  .container{
    width: 100%;
  }
}
@media(min-width: 1101px) and (max-width: 1600px){
  .forms{
    width: 60%;
  }
}
</style>