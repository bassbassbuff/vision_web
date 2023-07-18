<script setup>

import { computed, ref, onMounted, onUnmounted, watch } from 'vue'
import { useGeolocation } from '@/assets/js/useGeolocation'
//example components
import DefaultNavbar from "@/examples/navbars/NavbarDefault.vue";
import DefaultFooter from "@/examples/footers/FooterDefault.vue";
import PreFooterDefault from "@/examples/footers/PreFooterDefault.vue";


import { Loader } from "@googlemaps/js-api-loader"

 
    const { coords } = useGeolocation()
    const currPos = computed(() => ({
      lat: coords.value.latitude,
      lng: coords.value.longitude
    }))
    const otherPos = ref(null)


    const mapDiv = ref(null)
    let map = ref(null)


onMounted(async () => {
const loader = new Loader({
  apiKey: "AIzaSyDGLW4jHdko4GLks-09NpMAEc1v-erojbo",
  version: "weekly",
  // ...additionalOptions,
});
loader.load().then(async () => {
  const { Marker, Animation } = await google.maps.importLibrary("marker");
  const { Map } = await google.maps.importLibrary("maps");

  map.value = new google.maps.Map(mapDiv.value, {
    center: currPos.value,
    zoom: 6.5,
  });

  const nbi = new Marker({
    position: currPos.value,
    map: map.value,
    title: 'Vision Energy HQ',
  });

  const marker1 = new Marker({
    position: { lat: -4.047513466321188, lng: 39.66625816101843 },
    map: map.value,
    title: 'Office Location 2',
  });
   
  const marker2 = new Marker({
    position: { lat: -3.973537354111176, lng: 39.546095204156465 },
    map: map.value,
    title: 'Office Location 1',
  });

});
});
</script>

<template>
  <div class="container position-sticky z-index-sticky top-0">
    <div class="row">
      <div class="col-12">
        <DefaultNavbar
          :sticky="true"         
        />
      </div>
    </div>
  </div>
  <section class="py-sm-7 py-5 position-relative">
    <div class="container">
      <div class="row">
        <div class="col-12 mx-auto">          
          <div ref="mapDiv" class="row py-12">
            
              
            </div>
          </div>
        </div>
      </div>
      <PreFooterDefault />
      <DefaultFooter />    
  </section>
</template>