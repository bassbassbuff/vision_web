<script setup>
import DefaultCounterCard from "../../../examples/cards/counterCards/DefaultCounterCard.vue";
</script>

<template>
  <section class="pt-3 pb-4" id="count-stats">
    <div class="container">
      <div class="row">
        <div class="col-lg-9 z-index-2 border-radius-xl mx-auto py-3">
          <div class="row">
            <div class="col-md-4 position-relative">
              <DefaultCounterCard
                color="success"
                title="Industry Sectors"
                description="Under this segment, we supply LPG in industrial sectors such as Steel, 
                Automotive, Ceramic, Glass, Pharmaceuticals, Aerosol, Paper and Textile."
                :count="70"
                suffix="+"
                :duration="3000"
                divider="vertical"
              />
            </div>
            <div class="col-md-4 position-relative">
              <DefaultCounterCard
                color="success"
                title="Amaan Gas Retail Outlets"
                description="We have a strong spread of Amaan Gas retail outlets along with a wide
                network of distributors who sell our products to domestic and commercial customers."
                :count="1500"
                suffix="+"
                :duration="3000"
                divider="vertical"
              />
            </div>
            <div class="col-md-4">
              <DefaultCounterCard
                color="success"
                title="LPG Installations"
                description="Reticulation in Hotels, Apartments, Schools, Malls and Restaurants."
                :count="150"
                suffix="+"
                :duration="3000"
              />
            </div>           
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
