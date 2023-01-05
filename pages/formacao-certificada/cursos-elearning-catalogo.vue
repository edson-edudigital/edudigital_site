<template>
  <main>
    <Banner
    :title="$translate().formacao_certificada.banner.title2"
      :background-image="'https://edudigital.pt//images/top-plataformaseLearning%2020210318.png'"
      :button-action-text="$translate().formacao_certificada.banner.buttonText2"
      :button-action-href="'/fale-connosco'"
      :columns-template="'2fr 1fr'"
    >
      <template #text>
        {{$translate().formacao_certificada.banner.text2}}
      </template>
    </Banner>

    <Section :id="'curso-elearning-catalogo'" :flex="'column'">
      <Title :title="'Catálogo de cursos eLearning'" />

      <div class="catalogo-group">
        <Catalogo
          v-for="(catalogo, i) in catalogos"
          :key="i + $id"
          :img="catalogo.img"
          :title="catalogo.title"
        >
          {{ catalogo.text }}
        </Catalogo>
      </div>
    </Section>
  </main>
</template>

<script>
import Catalogo from '../../components/elements/catalogo.vue'
import Section from '~/components/sections/section.vue'
import Title from '~/components/elements/title.vue'
import FormacaoCertificadaController from '~/controllers/FormacaoCertificadaController'

export default {
  components: { Section, Title, Catalogo },
  data() {
    return {
      catalogos: FormacaoCertificadaController.cursoElearningCatalogo.catalogos,
    }
  },
}
</script>

<style>
.catalogo-group {
  margin-top: 40px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  row-gap: 50px;
}

@media screen and (max-width: 950px) {
  .catalogo-group {
    justify-content: center !important;
  }
}
</style>
