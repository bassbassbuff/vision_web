<script setup>
import { onMounted, onUnmounted } from "vue";

//example components
import NavbarDefault from "../..//examples/navbars/NavbarDefault.vue";
import DefaultFooter from "../../examples/footers/FooterDefault.vue";
import Header from "../../examples/Header.vue";
import FilledInfoCard from "../../examples/cards/infoCards/FilledInfoCard.vue";

//Vue Material Kit 2 components
import MaterialSocialButton from "@/components/MaterialSocialButton.vue";
import MaterialBadge from "@/components/MaterialBadge.vue";


// sections
import PresentationCounter from "./Sections/PresentationCounter.vue";
import PresentationPages from "./Sections/PresentationPages.vue";
import PresentationExample from "./Sections/PresentationExample.vue";
import data from "./Sections/Data/designBlocksData";
import BulkLpg from "./Components/BulkLpg.vue";
import RetailLpg from "./Components/RetailLpg.vue";
import Hospitality from "./Components/Hospitality.vue";
import InstallationsForLpg from "./Components/InstallationsForLpg.vue";
import PresentationTestimonials from "./Sections/PresentationTestimonials.vue";
import PresentationInformation from "./Sections/PresentationInformation.vue";

//images
import vueMkHeader from "@/assets/img/vue-mk-header.png";
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
      class="page-header min-vh-75"
      :style="`background-image: url(${vueMkHeader})`"
      loading="lazy"
    >
    <!-- <div class="bg-gradient-success position-relative mx-n3 overflow-hidden">
      <img
        src="@/assets/img/shapes/pattern-lines.svg"
        alt="pattern-lines"
        class="position-absolute start-0 top-md-0 w-100 opacity-6"
      />
      <div
        class="container pb-lg-8 pb-7 pt-5 postion-relative z-index-2 position-relative"
      >
        <div class="row">
          <div class="col-md-7 mx-auto text-center">
            <span class="badge bg-gradient-dark mb-2">Pricing</span>
            <h3 class="text-white">Ready to get Material Kit?</h3>
            <p class="text-white">
              Based on the license you get, you will have direct access to our
              team <br />
              of developers who built the product.
            </p>
          </div>
        </div>
      </div>
    </div> -->


      <div class="container">
        <div class="row">
          <div class="col-lg-7 text-center mx-auto position-relative bg-gradient-faded-white border-radius-lg">
            <img
              src="@/assets/img/vision_logo-07.png"
              alt="vission-logo"
              class=""
            />            
          </div>
        </div>
      </div>
    </div>
  </Header>

  <div class="card card-body blur shadow-blur mx-3 mx-md-4 mt-n6">
    <PresentationCounter />
    <PresentationInformation />

    <div class="container">
      <div class="row">
        <div class="row justify-content-center text-center my-sm-5">
          <div class="col-lg-6">
            <MaterialBadge class="mb-3 bg-[#3ecabf]"
              ><h2 class="text-white mb-0">Our Services</h2></MaterialBadge
            >            
            <p class="lead">
              Vision Energy Limited is currently continuing to invest in a number of
              projects which are aimed at establishing a virtuous future through
              improving eﬃciency, reducing distribution cost, ensuring availability
              and reliability and widening product access.
            </p>
          </div>
        </div>
      </div>
    </div>

    <BulkLpg />
    <RetailLpg />
    <InstallationsForLpg/>
    <Hospitality />
    <!-- <PresentationExample :data="data" /> -->
    <!-- <PresentationPages /> -->
    

    <!-- <div class="container">
      <div class="row">
        <div class="col-lg-4">
          <FilledInfoCard
            class="p-4"
            :color="{ text: 'white', background: 'bg-gradient-success' }"
            :icon="{ component: 'flag', color: 'white' }"
            title="LPG Hospitality"
            description="Check the possible ways of working with our product and the necessary files for building your own project."
            :action="{
              route:
                '',
              label: { text: 'Let\'s start', color: 'white' }
            }"
          />
        </div>
        <div class="col-lg-4">
          <FilledInfoCard
            class="px-lg-1 mt-lg-0 mt-4 p-4"
            height="h-100"
            :icon="{ component: 'precision_manufacturing', color: 'visiongreen' }"
            title="LPG Products"
            description="Check the possible ways of working with our product and the necessary 
            files for building your own project."
            :action="{
              route:
                '',
              label: { text: 'Read more' }
            }"
          />
        </div>
        <div class="col-lg-4">
          <FilledInfoCard
            class="p-4"
            :color="{ text: 'white', background: 'bg-gradient-success' }"
            :icon="{ component: 'flag', color: 'white' }"
            title="LPG Hospitality"
            description="Check the possible ways of working with our product and the necessary 
            files for building your own project."
            :action="{
              route:
                '',
              label: { text: 'Let\'s start', color: 'white' }
            }"
          />
        </div>
      </div>
    </div> -->
    <PresentationTestimonials />

    <div
      class="container-fluid mt-sm-5 border-radius-xl"
      :style="{
        background: 'linear-gradient(195deg, rgb(66, 66, 74), rgb(25, 25, 25))'
      }"
    >
      <div
        class="page-header py-6 py-md-5 my-sm-3 mb-3 border-radius-xl"
        :style="{
          backgroundImage: `url(${wavesWhite})`
        }"
        loading="lazy"
      >
        <span class="mask bg-gradient-dark"></span>
        <div class="container">
          <div class="row">
            <div class="d-flex justify-content-center p-5">
              <div class="col-lg-8 ms-lg-5 text-center">
                <h3 class="text-white">
                  We would love to hear from you
                </h3>
                <!-- <p class="text-white text-md">
                  Cause if you do, it can be yours for FREE. Hit the button
                  below to navigate to Creative Tim where you can <br />
                  find the Design System in HTML. Start a new project or give an
                  old Bootstrap project a new look!
                </p> -->

                <a
                  
                  class="btn btn-sm mb-0 bg-gradient-success px-5 py-3 mt-4"
                  >Send Message</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- <div class="container">
      <div class="row">
        <div class="d-flex flex-column w-100 text-center p-5 mb-8">
          <h3>Available on these technologies</h3>
          <div class="d-flex justify-content-center mt-3 flex-wrap">
            <a
              href="https://www.creative-tim.com/product/material-kit"
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="Bootstrap 5 - Most popular front-end component library"
            >
              <img
                :src="logoBootstrap"
                alt="title"
                loading="lazy"
                :style="{ height: '90px' }"
              />
            </a>
            <a
              class="opacity-5 ms-3"
              href="#"
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="Coming Soon"
            >
              <img
                :src="logoTailwind"
                alt="title"
                loading="lazy"
                :style="{ height: '90px' }"
              />
            </a>
            <a
              href="https://www.creative-tim.com/product/vue-material-kit-pro"
              class="mx-3"
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="Vue.js - Is a Progressive JavaScript Framework"
            >
              <img
                :src="logoVue"
                alt="title"
                loading="lazy"
                :style="{ height: '90px' }"
              />
            </a>
            <a
              class="opacity-5"
              href="#"
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="Coming Soon"
            >
              <img
                :src="logoAngular"
                alt="title"
                loading="lazy"
                :style="{ height: '90px' }"
              />
            </a>
            <a
              href="https://www.creative-tim.com/product/material-kit-react-pro"
              class="mx-3"
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="React – A JavaScript library for building user interfaces"
            >
              <img
                :src="logoReact"
                alt="title"
                loading="lazy"
                :style="{ height: '90px' }"
              />
            </a>
            <a
              class="opacity-5"
              href="#"
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="Coming Soon"
            >
              <img
                :src="logoSketch"
                alt="title"
                loading="lazy"
                :style="{ height: '90px' }"
              />
            </a>
          </div>
        </div>
      </div>
    </div> -->
    <div class="py-5">
      <div class="container">
        <div class="row">
          <div class="col-lg-5 ms-auto">
            <h4 class="mb-1">Thank you for your support!</h4>
            <p class="lead mb-0">We deliver the best LPG products</p>
          </div>
          <div class="col-lg-5 me-lg-auto my-lg-auto text-lg-end mt-5">
            <MaterialSocialButton
              route="https://twitter.com/"
              component="twitter"
              color="twitter"
              label="Tweet"
            />
            <MaterialSocialButton
              route="https://www.facebook.com/"
              component="facebook-square"
              color="facebook"
              label="Share"
            />
            <MaterialSocialButton
              route=""
              component="pinterest"
              color="pinterest"
              label="Pin it"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
  <DefaultFooter />
</template>
