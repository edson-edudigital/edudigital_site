<template>
  <main>
    <Banner
    :title="$translate().formacao_certificada.banner.title1"
      :background-image="'https://edudigital.pt/images/bigstock-Two-Smiling-Businessmen-Or-Pro-241216258%20.jpg'"
      :button-action-text="$translate().formacao_certificada.banner.buttonText1"
      :button-action-href="'/fale-connosco'"
      :columns-template="'2fr 1fr'"
    >
      <template #text>
        {{$translate().formacao_certificada.banner.text1}}
      </template>
    </Banner>

    <VantagemServicos
      :id="'consultoria-pedagogica-formacao-vantagem'"
      :vantagens="vantagem"
      :background="'#D35640'"
      :color="'#fff'"
      :title="'Serviços e Vantagens'"
    />

    <Contactform />
  </main>
</template>

<script>
import Catalogo from '../../components/elements/catalogo.vue'
import Section from '~/components/sections/section.vue'
import Title from '~/components/elements/title.vue'
import FormacaoCertificadaController from '~/controllers/FormacaoCertificadaController'
import VantagemServicos from '~/components/elements/vantagemServicos.vue'

export default {
  components: { Section, Title, Catalogo, VantagemServicos },
  data() {
    return {
      vantagem:
        FormacaoCertificadaController.consultoriaPedagogicaFormacao.vantagem,
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
