

<script setup>
import { onMounted, onUnmounted, onBeforeMount } from "vue";
import { useRoute, useRouter } from "vue-router"; // Import the router functions




//example components
import DefaultNavbar from "../../../examples/navbars/NavbarDefault.vue";
import DefaultFooter from "../../../examples/footers/FooterDefault.vue";

//image
import bg0 from "@/assets/img/bg9.jpg";

//dep
import Typed from "typed.js";

//sections
import Information from "./Sections/AboutInformation.vue";
import AboutTeam from "./Sections/AboutTeam.vue";
import Featuring from "./Sections/AboutFeaturing.vue";
import Newsletter from "./Sections/AboutNewsletter.vue";

//   // const route = useRoute(); // Get the current route
const router = useRouter(); // Get the router instance
// // Add a beforeEach navigation guard to scroll to the top on every route change
// const scrollBehavior = () => {
//   window.scrollTo(0, 0);
// };

// router.beforeEach((to, from, next) => {
//   // Call the scrollBehavior function before every route change
//   scrollBehavior();
//   next();
// });

const onScroll = () => {
    const bottomOfWindow = window.innerHeight + window.scrollY >= document.documentElement.offsetHeight;

    if (bottomOfWindow) {
      // Navigate to another route using router-link
      router.push({ name: 'mission' }); // Replace with your route name
    }
  };

const body = document.getElementsByTagName("body")[0];
//hooks

onBeforeMount(() => {
  const bottomOfWindow = window.innerHeight + window.scrollY >= document.documentElement.offsetHeight;
//   // Scroll to the top before the component is mounted
//   console.log("beforeMount")
if (bottomOfWindow) {
      // Scroll to the top of the page
      window.scrollTo(0, 0);
}
});
//   }
// });



onMounted(() => {
  body.classList.add("about-us");
  body.classList.add("bg-gray-200");

  if (document.getElementById("typed")) {
    // eslint-disable-next-line no-unused-vars
    var typed = new Typed("#typed", {
      stringsElement: "#typed-strings",
      typeSpeed: 90,
      backSpeed: 90,
      backDelay: 200,
      startDelay: 500,
      loop: true,
    });
  }


  // Attach the onScroll function to the scroll event
  window.addEventListener('scroll', onScroll);
    // Add afterEach navigation guard to remove the scroll event listener
  //   router.afterEach((to, from) => {
  //   window.removeEventListener('scroll', onScroll);
  // });
  // Scroll to the top when the component is mounted
  // if (window) {
  //   window.scrollTo(0, 0);
  // }
});

onUnmounted(() => {
    // Remove the event listener on unmount
  window.removeEventListener('scroll', onScroll);
  body.classList.remove("about-us");
  body.classList.remove("bg-gray-200");
});
</script>

<template>
  <DefaultNavbar
    :action="{
      route: '',
      // label: 'Buy Now',
      // color: 'btn-white',
    }"
    transparent
  />
  <header class="bg-gradient-dark">
    <div
      class="page-header min-vh-75"
      :style="{ backgroundImage: `url(${bg0})` }"
    >
      <span class="mask bg-gradient-dark opacity-6"></span>
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-8 text-center mx-auto my-auto">
            <h1 class="text-white">
              Who we are
            </h1>
            <!-- <h1 class="text-white">
              Work with amazing <span class="text-white" id="typed"></span>
            </h1> -->
            <!-- <div id="typed-strings"> -->
            <!-- <div id="">
              <h1>people</h1>
              <h1>products</h1> -->
              <!-- <h1>tool</h1> -->
            <!-- </div> -->
            <p class="lead mb-4 text-white opacity-8">
              Vision Energy Limited is a Kenya based integrated gas entity aiming to
              be the leader within the LPG industry throughout the east and central
              africa regions.
              Our trading presence is underpinned by a complementary infrastructure: 
              currently storage, distribution and a marketing network. In all our
              physical operations we seek to work with partners who share our com
              mitment to high international standards of operation. The 
              infrastructure upon which we rely, is subject to thorough due diligence processes.
              As physical traders, we gain ﬁrst hand experience of economic 
              fundamentals as they play out on the ground.
            </p>
            <!-- <button type="submit" class="btn bg-white text-dark">
              Create Account
            </button> -->
            <h6 class="text-white mb-2 mt-5">Find us on</h6>
            <div class="d-flex justify-content-center">
              <a href="javascript:;"
                ><i class="fab fa-facebook text-lg text-white me-4"></i
              ></a>
              <a href="javascript:;"
                ><i class="fab fa-instagram text-lg text-white me-4"></i
              ></a>
              <a href="javascript:;"
                ><i class="fab fa-twitter text-lg text-white me-4"></i
              ></a>
              <a href="javascript:;"
                ><i class="fab fa-google-plus text-lg text-white"></i
              ></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
  <div class="card card-body shadow-xl mx-3 mx-md-4 mt-n6">
    <!-- <Information /> -->
    <AboutTeam />
    <Featuring />
    <Newsletter />
  </div>
  <DefaultFooter />
</template>
