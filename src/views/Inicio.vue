<template lang="pug">
section
  BannerPrincipal.mb-5
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 1. Presentación

    p El SENA, le da la bienvenida al Programa de tecnología en Desarrollo de Procesos de Mercadeo, soportado en el reiterado cambio, en las preferencias de los consumidores, debido a la evolución tecnológica y la insistente lucha de las empresas, por   obtener   la   fidelización   de   sus   usuarios que ha ocasionado que hoy en día, se encuentren productos y servicios capaces de satisfacer cualquier necesidad, por lo cual, entender las particularidades del mercadeo, es la clave, para el éxito de toda organización (Puente, 2006).
      br
    p Con este programa usted desarrollará las competencias que le permitirán desenvolverse en el apoyo para adelantar estudios y estrategias de mercadeo, desarrollo de productos, aportar en el manejo de la comunicación corporativa y actualizar información de proyectos de mercadeo, acordes con los planes estratégicos y políticas de la organización.

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 2. Perfil<br>de ingreso
    p.mb-3 Para responder a las dinámicas de los procesos inherentes al mercadeo, el SENA oferta, la Tecnología en Desarrollo de Procesos de Mercadeo, con la finalidad de que, las acciones de marketing aplicadas por las organizaciones se conviertan en una actividad empresarial proactiva, inteligente y dinámica; en donde el empresario, debe romper paradigmas para aceptar que esta área, impacte las demás áreas funcionales de la empresa y se convierta, en el “alma de la organización” (Herrera, 2013).
    p.mb-3 Teniendo en cuenta, que el mercadeo, “es el proceso de desarrollar, promover y distribuir productos, con el fin de responder a las exigencias y deseos de los clientes”(Louis Scheeider  Farese, 2001); es innegable, la necesidad de que toda organización  comercial, cuente con, Asistentes de mercadeo, publicidad y comunicaciones, que intervengan en el desarrollo de estrategias de mercadeo; premisa  con  la  cual,  parecen  estar  de acuerdo los empresarios; ya que las ocupaciones relacionadas con mercadeo y ventas reportan un mayor número de vacantes colocados y está dentro de las diez principales ocupaciones, de la mesa sectorial (APE -SENA, 2017).
    p Finalmente, las oportunidades de vinculación laboral para los Asistentes de mercadeo, publicidad y comunicaciones, son prometedoras, si se tiene en cuenta, el incremento en la demanda de personal capacitado, en ocupaciones relacionadas con los servicios; la cual representó, el 55% del total de vacantes registradas en el Servicio público de empleo del SENA –APE, en el año 2017, que si se compara, con la cifra del año inmediatamente anterior, se observó una variación positiva del 4,01%  (Observatorio SPE -SENA, 2017).
  
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 3. Perfil <br> de egreso
    p El egresado del programa Tecnología en desarrollo de procesos de mercadeo es un talento humano formado integralmente bajo el enfoque por competencias con capacidad para apoyar en la realización de estudios y estrategias de mercadeo, desarrollo de productos, aportar en el manejo de la comunicación corporativa y actualizar información de  proyectos  de  mercadeo,  acordes  con  los  planes  estratégicos y políticas de la organización; con el fin de proporcionar herramientas que posibiliten el proceso de toma de decisiones y lograr  mayor eficiencia, en los procesos de mercadeo, de las organizaciones; con un alto sentido de responsabilidad en el desempeño de sus funciones. El aprendiz, deberá desarrollar “habilidades blandas”, como la comunicación asertiva, proactividad y trabajo en equipo.   Podrá desempeñarse en empresas de servicios, comerciales e industriales, de carácter público o privado y emprender creando unidades de negocio para atención a pymes y micro pymes, en cargos de Asistentes de mercadeo, publicidad y comunicaciones.
  
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 3. Estrategia<br>metodológica

    p Centrada en la construcción de autonomía para garantizar la calidad de la formación en el marco de la formación por competencias, el aprendizaje por proyectos y el uso de técnicas didácticas activas que estimulan el pensamiento para la resolución de problemas simulados y reales; soportadas en la utilización de las tecnologías de la información y la comunicación, integradas, en ambientes virtuales de aprendizaje, que en todo caso recrean el contexto productivo y vinculan al aprendiz con la realidad cotidiana y el desarrollo de las competencias. 
      br
      br
      | Igualmente, debe estimular de manera permanente la autocrítica y la reflexión del aprendiz sobre el que hacer y los resultados de aprendizaje que logra a través de la vinculación activa de las cuatro fuentes de información para la construcción de conocimiento:
      br
      ul
        li -	El instructor - Tutor
        li -	El entorno
        li -	Las TIC
        li -  El trabajo colaborativo

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
