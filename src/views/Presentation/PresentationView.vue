<script setup>
import { onMounted, onUnmounted } from "vue";

//example components
import NavbarDefault from "../..//examples/navbars/NavbarDefault.vue";
import DefaultFooter from "../../examples/footers/FooterDefault.vue";
import Header from "../../examples/Header.vue";
import FilledInfoCard from "../../examples/cards/infoCards/FilledInfoCard.vue";
import AboutUsOption from "@/views/LandingPages/Components/AboutUsOption.vue";



//Vue Material Kit 2 components
import MaterialSocialButton from "@/components/MaterialSocialButton.vue";

// sections
import PresentationCounter from "./Sections/PresentationCounter.vue";
import PresentationPages from "./Sections/PresentationPages.vue";
import PresentationExample from "./Sections/PresentationExample.vue";
import data from "./Sections/Data/designBlocksData";
import BuiltByDevelopers from "./Components/BuiltByDevelopers.vue";
import PresentationTestimonials from "./Sections/PresentationTestimonials.vue";
import PresentationInformation from "./Sections/PresentationInformation.vue";

//images
import vueMkHeader from "@/assets/img/fondo-3.jpeg";
import wavesWhite from "@/assets/img/waves-white.svg";
import logoBootstrap from "@/assets/img/logos/bootstrap5.jpg";
import logoTailwind from "@/assets/img/logos/icon-tailwind.jpg";
import logoVue from "@/assets/img/logos/vue.jpg";
import logoAngular from "@/assets/img/logos/angular.jpg";
import logoReact from "@/assets/img/logos/react.jpg";
import logoSketch from "@/assets/img/logos/sketch.jpg";

//hooks
const body = document.getElementsByTagName("body")[0];
onMounted(() => {
  body.classList.add("presentation-page");
  body.classList.add("bg-gray-200");
});
onUnmounted(() => {
  body.classList.remove("presentation-page");
  body.classList.remove("bg-gray-200");
});
</script>

<template>
  <div class="container position-sticky z-index-sticky top-0">
    <div class="row">
      <div class="col-12">
        <NavbarDefault :sticky="true" />
      </div>
    </div>
  </div>
  <Header>
    <div
      class="page-header min-vh-100"
      :style="`background-image: url(${vueMkHeader})`"
      loading="lazy"
    >
      <div class="container">
        <div class="row">
          <div class="col-lg-7 text-start mx-auto position-end">
            <h1
              class="text-white pt-3 mt-n5 me-2"
              :style="{ display: 'inline-block ' }"
            >
              Catálogo de Ventas
            </h1>
            <p class="lead text-white px-5 mt-3" :style="{ fontWeight: '500' }">
              Descubre una experiencia<br>única de compras, donde la <br>
              <h4 class="text-white"><strong>innovación & calidad</strong></h4>
              se unen para satisfacer<br> tus necesidades.
            </p>
          </div>
        </div>
      </div>
    </div>
  </Header>

  <div class="card card-body blur shadow-blur mx-3 mx-md-4 mt-n6">
    <section class="py-9">
    <div class="container">
      <div class="row">
        <div class="col-lg-6 my-auto">
          <h3>Read More About Us</h3>
          <p class="pe-5">
            Pain is what we go through as we become older. We get insulted by
            others, lose trust for those others. We get back stabbed by friends.
            It becomes harder for us to give others a hand.
          </p>
          <a href="javascript:;" class="text-success icon-move-right"
            >More about us
            <i class="fas fa-arrow-right text-sm ms-1"></i>
          </a>
        </div>
        <div class="col-lg-6 mt-lg-0 mt-5 ps-lg-0 ps-0">
          <AboutUsOption
            icon="mediation"
            content="It becomes harder for us to give others a hand.<br />
            We get our heart broken by people we love."
          />
          <AboutUsOption
            icon="settings_overscan"
            content="As we live, our hearts turn colder.<br />
            Cause pain is what we go through as we become older."
          />

          <AboutUsOption
            icon="token"
            content="When we lose family over
            time. <br />
            What else could rust the heart more over time? Blackgold."
          />
        </div>
      </div>
    </div>
  </section>
    <PresentationCounter />
    <PresentationInformation />
  </div>
  <DefaultFooter />
</template>
