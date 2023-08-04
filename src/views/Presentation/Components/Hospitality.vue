<script setup>

//images
import bg_hospitality from "@/assets/img/bg_hospitality.jpg";

</script>
<template>
  <div class="container mt-sm-5">
    <div
      class="page-header py-6 py-md-5 my-sm-3 mb-3 border-radius-xl"
      :style="`background-image: url(${bg_hospitality})`"
      loading="lazy"
    >
      <span class="mask bg-gradient-dark"></span>
      <div class="container">
        <div class="row">
          <div class="col-lg-6 ms-lg-5">
            <h4 class="text-white">Hospitality</h4>
            <h1 class="text-white">LPG Hospitality</h1>
            <p class="lead text-white opacity-8">
              We oﬀer LPG hospitality services; Whereby entities that own cylinder
              brands and lack storage and reﬁlling facilities can store and reﬁll their 
              cylinders at our various depots across the country.
            </p>
            <a
              href=""
              class="text-white icon-move-right"
            >
              Read more
              <i class="fas fa-arrow-right text-sm ms-1"></i>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
