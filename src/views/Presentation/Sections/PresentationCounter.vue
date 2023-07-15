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
                title="Bulk LPG"
                description="High quality Bulk LPG gas ideal for industrial and commercial consumers 
                spanning from plastic manufacturing, steel shaping, glass making, hospitals, 
                hotels, aerosols manufacturing, 
                just to name a few. We have the capacity to fulfil your LPG gas requirements."
                :count="70"
                suffix="+"
                :duration="3000"
                divider="vertical"
              />
            </div>
            <div class="col-md-4 position-relative">
              <DefaultCounterCard
                color="success"
                title="Retail"
                description="High quality Bulk LPG gas ideal for industrial and commercial consumers 
                spanning from plastic manufacturing, steel shaping, glass making, hospitals, 
                hotels, aerosols manufacturing, 
                just to name a few. We have the capacity to fulfil your LPG gas requirements."
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
                description="High quality Bulk LPG gas ideal for industrial and commercial consumers 
                spanning from plastic manufacturing, steel shaping, glass making, hospitals, 
                hotels, aerosols manufacturing, 
                just to name a few. We have the capacity to fulfil your LPG gas requirements."
                :count="15"
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
