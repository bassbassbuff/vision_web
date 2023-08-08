<script setup>
// example component
import ValuesCard from "@/examples/cards/valuesCards/ValuesCard.vue";

// images
import emma from "@/assets/img/pitch.png";
import william from "@/assets/img/mission2.jpg";
import ivana from "@/assets/img/ivana-squares.jpg";
import marquez from "@/assets/img/ivana-square.jpg";
</script>

<template>
  <section class="pb-5 position-relative bg-gradient-dark mx-n3">
    <div class="container">
      <!-- <div class="row">
        <div class="col-md-8 text-start mb-5 mt-5">
          <h3 class="text-white z-index-1 position-relative">
            The Executive Team
          </h3>
          <p class="text-white opacity-8 mb-0">
            There’s nothing I really wanted to do in life that I wasn’t able to
            get good at. That’s my skill.
          </p>
        </div>
      </div> -->
      <div class="row">
        <!-- <div class="page-header min-vh-75">
          <ValuesCard
            class="mt-4"
            :image="emma"
            :profile="{ name: 'Vision', link: 'javascript:;' }"
            description="To be the leader in LPG importation, exportation
            and transportation in East and Central Africa.."
            
          />
        </div> -->
        <div class="page-header min-vh-75">
          <ValuesCard
            class="mt-4"
            :image="emma"
            :profiles="[
                        { name: 'Professionalism', 
                          link: 'javascript:;', 
                          description: 'At our company, professionalism is at the heart of everything we do. We hold ourselves to the highest standards of conduct, expertise, and accountability. Our team is dedicated to delivering exceptional service and maintaining a professional demeanor in all interactions.' },
                        { name: 'Integrity & Innovation', 
                          link: 'javascript:;', 
                          description: 'Integrity is the foundation of our company. We are committed to conducting our business with honesty, transparency, and ethical behavior. We also embrace innovation, constantly seeking new and better ways to serve our customers and improve our processes.' },
                        { name: 'Teamwork', 
                        link: 'javascript:;', 
                        description: 'Collaboration and unity define our approach. We believe that working together as a team is essential to achieving excellence. Each member of our staff contributes their unique skills and expertise, creating a synergy that drives our success.' },
                        { name: 'Customer Centric ', 
                        link: 'javascript:;', 
                        description: 'Our customers are at the center of everything we do. We prioritize their needs, preferences, and satisfaction. We aim to provide tailored solutions and outstanding service that exceed their expectations, building long-lasting relationships.' },
                        { name: 'Honesty', 
                        link: 'javascript:;', 
                        description: 'Honesty is a cornerstone of our operations. We believe in straightforward and truthful communication with our customers, partners, and colleagues. By upholding the value of honesty, we foster trust and maintain the integrity of our business relationships.' },
  
                          // Add more profile objects as needed
  ]"
            
          />
        </div>
        
        
        <!-- <div class="col-lg-6 col-12">
          <HorizontalMissionCard
            class="mt-lg-4 mt-5"
            :image="william"
            :profile="{ name: 'Mission', link: 'javascript:;' }"
            description="Our purpose is to fulﬁll your LPG requirements at
            the best aﬀordable rates.."
          />
        </div> -->
      </div>
      <!-- <div class="row mt-4">
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-4 z-index-2"
            :image="ivana"
            :profile="{ name: 'Ivana Flow', link: 'javascript:;' }"
            :position="{ label: 'Athlete', color: 'success' }"
            description="Artist is a term applied to a person who engages in an
                    activity deemed to be an art."
          />
        </div>
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-lg-4 mt-5 z-index-2"
            :image="marquez"
            :profile="{ name: 'Marquez Garcia', link: 'javascript:;' }"
            :position="{ label: 'JS Developer', color: 'success' }"
            description="Artist is a term applied to a person who engages in an
                    activity deemed to be an art."
          />
        </div>
      </div> -->
    </div>
  </section>
</template>
