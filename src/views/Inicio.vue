<template lang="pug">
section
  BannerPrincipal.mb-5


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 1. Presentación

    p.mb-3 El Servicio Nacional de Aprendizaje (SENA) articulado con el Ministerio de Industria, Comercio y Turismo (MinCIT) y el Ministerio de las Tecnologías de la Información y las Comunicaciones (MinTIC) se unen ante la emergencia que atraviesa nuestro país (Covid-19) implementando una estrategia de asistencia técnica virtual por medio de un proceso de consultoría, que impacte las MiPymes a través de transformación digital y búsqueda de nuevas oportunidades de negocios, implementando la estrategia #MiPymesetransforma “Empresas con Mentalidad TIC”.
    
    p.mb-3 La presente formación le ayuda a conocer la metodología de extensionismo tecnológico y la Estrategia #MipymeSeTransforma, la cual pretende transformar los procesos de digitalización de las MiPymes colombianas, en el actual contexto económico y tecnológico, para cumplir con indicadores y retos que las lleven a innovar en estrategias y proyectos de transformación y apropiación digital, con lo cual logren diferenciación y competitividad en sus sectores y ofertas de valor; sobre todo en esta época de problemáticas en la salud pública con el Covid-19, se hace necesario que las empresas puedan utilizar de mejor manera las TIC. 

    
    p.mb-3 Esperamos que con estos recursos a su disposición puedan aprender sobre estos procesos y con ello puedan comprender la implementación de la metodología de extensionismo tecnológico.

    
    p.mb-3 ¡Bienvenidos!


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 2. Justificación<br>del programa

    p.mb-3 La transformación digital es un proceso relevante para las empresas en el mundo y en el caso de Colombia desde su proceso actual de cambio tecnológico digital en la actual recuperación económica –reapertura y reactivación– requieren de este tipo de transformación social y tecnológica en lo digital para las MiPymes.
    
    p.mb-3 El programa de Extensionismo Tecnológico del SENA busca que los profesionales consultores que trabajan la metodología desde los roles de Gestor Consultor y Extensionista Tecnológico desarrollen competencias en el marco de la implementación de la estrategia y la gestión empresarial e informática requerida para el cambio de la transformación digital en las empresas en Colombia.
    
    p.mb-3 El presente programa de formación complementaria en la estrategia MiPyme Se transforma ofrece herramientas conceptuales y prácticas a los consultores sobre el programa del SENA para acompañar a las empresas de los diferentes sectores económicos y regiones del país, en el mejoramiento de la productividad a partir de innovaciones de productos, procesos y/o servicios y adopción de tecnologías informáticas asociadas aumentando la productividad y la competitividad de las empresas. 


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 3. Competencia<br>a desarrollar

    p #[strong 240101015] - Diagnosticar situación problema según metodologías y procedimiento técnico.
    p.mb-0 #[strong 240101017] - Dirigir implementación de soluciones según requerimientos técnicos y plan de intervención.


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 4.	Perfil<br>de ingreso

    p Tener título profesional en ingeniería, ciencias económicas, administrativas o afines. Experiencia certificada de mínimo 3 años en participación en proyectos relacionados con consultoría, articulación, apropiación y/o divulgación de procesos de transformación digital en sistemas de gestión, herramientas de productividad, mejoramiento continuo y/o desarrollo e innovación en micros, pequeñas y medianas (MiPymes).


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 5.	Perfil<br>de egreso

    p No aplica.


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 6. Estrategia<br>metodológica

    p.mb-3 Centrada en la construcción de autonomía para garantizar la calidad de los procesos formativos en el marco de la formación por competencias, el aprendizaje por proyectos y el uso de técnicas didácticas activas que estimulan el pensamiento para la resolución de problemas simulados y reales; soportadas en el utilización de las tecnologías de la información y la comunicación, integradas, en ambientes abiertos y pluritecnológicos que, en todo caso, recrean el contexto productivo y vinculan al aprendiz con la realidad cotidiana y el desarrollo de las competencias.

    p.mb-3 Igualmente, debe estimular de manera permanente la autocrítica y la reflexión del aprendiz sobre el que hacer y los resultados de aprendizaje que logra a través de la vinculación activa de las cuatro fuentes de información para la construcción de conocimiento:

    p.mb-0 •	El instructor – Tutor.
    p.mb-0 •	El entorno.
    p.mb-0 •	Las TIC.
    p.mb-0 •	El trabajo colaborativo.



  //- Créditos
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 Créditos

    CreditosComp

  Footer
  

</template>
<script>
import { menuPrincipal } from '../config/global'
import BannerPrincipal from '../components/plantilla/BannerPrincipal'
import CreditosComp from '../components/plantilla/CreditosComp'
import Footer from '../components/plantilla/Footer'
export default {
  name: 'Inicio',
  components: {
    BannerPrincipal,
    CreditosComp,
    Footer,
  },
  data: () => ({
    menuPrincipalData: menuPrincipal,
  }),
  computed: {
    desarrolloContenidosData() {
      const allMenuData = [
        ...this.menuPrincipalData.menu,
        ...this.menuPrincipalData.subMenu,
      ]
      return allMenuData.filter(item => item.desarrolloContenidos)
    },
  },
}
</script>

<style lang="sass" scoped>
.resultados-aprendizaje
  &__item
    margin-bottom: 20px
    &:last-child
      margin-bottom: 0

.desarrollo-contenidos
  &__item
    display: flex
    align-items: center
    justify-content: space-between
    margin-bottom: 25px
    padding: 5px
    border-radius: $base-border-radius

    &__texto
      display: flex
      align-items: center

    &__icono
      display: block
      background-color: $color-sistema-g
      font-size: 20px
      font-weight: $base-black-font-weight
      text-align: center
      padding: 10px
      line-height: 1em
      width: 40px
      margin-right: 15px

    &:last-child
      margin-bottom: 0

    &:hover
      background-color: $color-sistema-g
      font-weight: $base-black-font-weight
      color: $color-sistema-a
</style>
