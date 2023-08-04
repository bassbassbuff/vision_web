<script setup>
import DefaultReviewCard from "@/examples/cards/reviewCards/DefaultReviewCard.vue";
import PresentationContact from "./PresentationContact.vue";
</script>
<template>
  <section class="py-7">
    <div class="container">
      <div class="row">
        <div class="col-lg-6 mx-auto text-center">
          <h2 class="mb-0">Trusted by over</h2>
          <h2 class="text-gradient text-success mb-3">
            1,000+ dealers
          </h2>
          <p class="lead">
            Many Fortune companies, startups, universities and governmental
            institutions love Vision Energy products.
          </p>
        </div>
      </div>
      <div class="row mt-6">
        <DefaultReviewCard
          name="Nick Willever"
          date="1 day ago"
          review='"Vision Energy has helped us record tremendous growth 
          through the supply of high quality petroleum products at cost 
          effective rates. Their efficient delivery of product and quick 
          response to delays has ensured that we are operational round 
          the clock."'
          :rating="5.0"
        />
        <DefaultReviewCard
          class="ms-md-auto"
          color="bg-gradient-success"
          name="Shailesh Kushwaha"
          date="1 week ago"
          review='"As a result of Vision Energy efficiency,
           we have recorded a remarkable drop in our 
           operating expenses and this has led us to 
           invest additional capital into growing our 
           business. We therefore commend Vision Energy 
           for the excellent job they are doing and recommend 
           them to others looking for a petrol station 
           dealership partner."'
          :rating="5.0"
        />
        <PresentationContact/>
        <!-- <DefaultReviewCard
          name="Samuel Kamuli"
          date="3 weeks ago"
          review='"Vision Energy has helped us record tremendous growth 
          through the supply of high quality petroleum products at cost 
          effective rates. Their efficient delivery of product and quick 
          response to delays has ensured that we are operational round 
          the clock."'
          :rating="5.0"
        /> -->
      </div>
      <hr class="horizontal dark my-5" />
      <div class="row">
        <!-- <div class="col-lg-2 col-md-4 col-6 ms-auto">
          <img
            class="w-100 opacity-6"
            src="@/assets/img/logos/gray-logos/logo-apple.svg"
            alt="Logo"
          />
        </div> -->
        <div class="col-lg-3 col-md-4 col-6">
          <img
            class="w-100 opacity-6"
            src="@/assets/img/logos/gray-logos/logo-hunkar.svg"
            alt="Logo"
          />
        </div>
        <div class="col-lg-3 col-md-4 col-6">
          <img
            class="w-100 opacity-6"
            src="@/assets/img/logos/gray-logos/logo-hass.svg"
            alt="Logo"
          />
        </div>
        <div class="col-lg-3 col-md-4 col-6 ms-lg-0 ms-md-auto">
          <img
            class="w-100 opacity-6"
            src="@/assets/img/logos/gray-logos/logo-petrocity.svg"
            alt="Logo"
          />
        </div>
        <div class="col-lg-3 col-md-4 col-6 me-md-auto mx-md-0 mx-auto">
          <img
            class="w-100 opacity-6"
            src="@/assets/img/logos/gray-logos/logo-lakegas.svg"
            alt="Logo"
          />
        </div>
      </div>
    </div>
  </section>
</template>
