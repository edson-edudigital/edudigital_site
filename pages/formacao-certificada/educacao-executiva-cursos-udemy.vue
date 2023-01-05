<template>
    <div>
      <Banner
        :background-image="'https://edudigital.pt/images/bigstock-Two-Smiling-Businessmen-Or-Pro-241216258%20.jpg'"
        :title="$translate().formacao_certificada.banner.title3"
        :columns-template="'2fr 1fr'"
        :button-action-text="$translate().formacao_certificada.banner.buttonText3"
        :button-action-href="'/fale-connosco'"
      >
        <template #text>
          {{$translate().formacao_certificada.banner.text3}}
        </template>
      </Banner>
  
      <SectiondubleCartoon
        :id="'elearning-personalizado-design'"
        :background="'#fff'"
        :img="'https://edudigital.pt/home/images/Grupo_815.png'"
        :flex-direction="'row'"
        :color="'#616161'"
      >
        <template #text>
          <Title :title="'Cursos Udemy'" />
          <p>
            A EDUdigital é parceira oficial da Udemy Business; disponibiliza e integra em 
            plataformas, mais de 183.000 cursos produzidos por especialistas, sobre assuntos 
            técnicos e comportamentais. Os cursos da Udemy são projetados para especializar 
            formandos, aumentar a produtividade e dar competências técnicas em áreas de 
            conhecimento críticas.
          </p>
        </template>
      </SectiondubleCartoon>
  
      <VantagemServicos
        :id="'hosting-gerido-servicos-vantagens'"
        :vantagens="vantagens"
        :background="'#D35640'"
        :color="'#fff'"
        :title="'Serviços e Vantagens'"
      />
  
      <Contactform />
    </div>
  </template>
  
  <script>
  import FormacaoCertificadaController from '~/controllers/FormacaoCertificadaController'
  import VantagemServicos from '~/components/elements/vantagemServicos.vue'
  import Contactform from '~/components/contactform.vue'
  import SectiondubleCartoon from '~/components/sections/sectiondubleCartoon.vue'
  import Title from '~/components/elements/title.vue'
  export default {
    components: { VantagemServicos, Contactform, SectiondubleCartoon, Title },
    data() {
      return {
        vantagens: FormacaoCertificadaController.cursosUdemy.vantagens,
      }
    },
  }
  </script>
  
  <style></style>
  