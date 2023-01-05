<template>
  <div>
    <Banner
      :background-image="'	https://edudigital.pt/images/bigstock-Two-Smiling-Businessmen-Or-Pro-241216258%20.jpg'"
      
      :title ="$translate().apps_servicos_web.banner.title2" 
      :columns-template="'2fr 1fr'"
      :button-action-text="$translate().apps_servicos_web.banner.buttonText1"
      :button-action-href="'/fale-connosco'"
    >
      <template #text>
    
          {{$translate().apps_servicos_web.banner.text2}}
          
      </template>
    </Banner>

    <SectiondubleCartoon
      :id="'configuracao-avancada'"
      :background="'#fff'"
      :img="require('~/assets/img/cartoon/grp_apps_01_.png')"
      :flex-direction="'row'"
      :color="'#616161'"
    >
      <template #text>
        <Title :title="$translate().apps_servicos_web.software_integration.title" />
        <p>
          {{$translate().apps_servicos_web.advanced_configuration.text2}}
        </p>
      </template>
    </SectiondubleCartoon>

    <VantagemServicos
      :id="'integracao-migracao-dados-vantagens'"
      :vantagens="configAvancadaVantagens"
      :background="'#D35640'"
      :color="'#fff'"
      :title="'Serviços e Vantagens'"
    />

    <SectiondubleCartoon
      :id="'config-avancada-autenticacao'"
      :background="'#fff'"
      :img="'https://edudigital.pt/home/images/autenticaao-02.png'"
      :flex-direction="'row-reverse'"
      :color="'#616161'"
    >
      <template #text>
        <Title :title="'Sistemas de autenticação'" />
        <p>
          {{$translate().apps_servicos_web.autentication_systems.text2}}
        </p>
      </template>
    </SectiondubleCartoon>

    <VantagemServicos
      :id="'migracao-dados-vantagens'"
      :vantagens="autenticacaoVantagem"
      :background="'#D35640'"
      :color="'#fff'"
      :title="'Serviços e Vantagens'"
    />

    <Contactform />
  </div>
</template>

<script>
import VantagemServicos from '~/components/elements/vantagemServicos.vue'
import Contactform from '~/components/contactform.vue'
import SectiondubleCartoon from '~/components/sections/sectiondubleCartoon.vue'
import Title from '~/components/elements/title.vue'
import AppServicosWebController from '~/controllers/AppServicosWebController'
export default {
  components: { VantagemServicos, Contactform, SectiondubleCartoon, Title },
  data() {
    return {
      configAvancadaVantagens:
        AppServicosWebController.configuracaoAvancada.vantagem,
      autenticacaoVantagem:
        AppServicosWebController.configuracaoAvancada
          .configuracaoAvancadaAutenticacao.vantagens,
    }
  },
}
</script>

<style></style>
