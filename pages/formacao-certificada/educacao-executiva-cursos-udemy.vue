<template>
    <div>
      <Banner
        :background-image="'https://edudigital.pt/images/bigstock-Two-Smiling-Businessmen-Or-Pro-241216258%20.jpg'"
        :title="'Educação Executiva Nova SBE'"
        :columns-template="'2fr 1fr'"
        :button-action-text="'Agende a sua reunião'"
        :button-action-href="'/fale-connosco'"
      >
        <template #text>
            A EDUdigital é parceira da Universidade Nova de Lisboa - School of Business & 
            Economics e disponibiliza programas de formação dedicados às necessidades dos 
            executivos. São programas em diversas áreas adaptados aos objetivos e atividades de 
            profissionais e quadros médios e altos de empresas. Explore os 11 programas que temos 
            disponíveis.
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
  