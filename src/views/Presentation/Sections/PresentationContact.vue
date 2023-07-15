<script setup>
import { onMounted } from "vue";
//Vue Material Kit 2 components
import MaterialButton from "@/components/MaterialButton.vue";
import MaterialInput from "@/components/MaterialInput.vue";
import MaterialTextArea from "@/components/MaterialTextArea.vue";

// image
import bgContact from "@/assets/img/examples/blog2.jpg";

// tooltip
import setTooltip from "@/assets/js/tooltip";

// store
import { useAppStore } from "@/stores";
const store = useAppStore();

onMounted(() => {
  setTooltip(store.bootstrap);
});
</script>
<!-- <template>
  <section class="py-lg-5">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="card box-shadow-xl overflow-hidden mb-5">
            <div class="row">              
              <div class="col-lg-7">
                <form class="p-3" id="contact-form" method="post">
                  <div class="card-header px-4 py-sm-5 py-3">
                    <h2>Say Hi!</h2>
                    <p class="lead">We'd like to talk with you.</p>
                  </div>
                  <div class="card-body pt-1">
                    <div class="row">
                      <div class="col-md-12 pe-2 mb-3">
                        <MaterialInput
                          class="input-group-static mb-4"
                          label="My name is"
                          type="text"
                          placeholder="Full Name"
                        />
                      </div>
                      <div class="col-md-12 pe-2 mb-3">
                        <MaterialInput
                          class="input-group-static mb-4"
                          label="I'm looking for"
                          type="text"
                          placeholder="What you love"
                        />
                      </div>
                      <div class="col-md-12 pe-2 mb-3">
                        <MaterialTextArea
                          class="input-group-static mb-4"
                          placeholder="I want to say that..."
                          :rows="6"
                          >Your message</MaterialTextArea
                        >
                      </div>
                    </div>
                    <div class="row">
                      <div class="col-md-6 text-end ms-auto">
                        <MaterialButton
                          variant="gradient"
                          color="success"
                          type="submit"
                          class="mb-0"
                          >Send Message</MaterialButton
                        >
                      </div>
                    </div>
                  </div>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template> -->
<template>
  <div class="col-lg-4 col-md-8">
    <form class="p-3" id="contact-form" method="post">
      <!-- <div class="card-header px-4 py-sm-5 py-3">
        <h2>Dealer application</h2>
        <p class="lead">We'd like to talk with you.</p>
      </div> -->
      <div class="card-body pt-1">
        <div class="author">
          <div class="name">
            <h3
              class="mb-0 font-weight-bolder"
            >
              Dealer application
          </h3>
              <MaterialInput
                class="input-group-static mt-4 mb-4"
                label="My name is"
                type="text"
                placeholder="Full Name"
              />
              <MaterialInput
                class="input-group-static mb-4"
                label="My email is"
                type="text"
                placeholder="Email"
              />
              <MaterialInput
                class="input-group-static mb-4"
                label="My number"
                type="text"
                placeholder="Phone"
              />
              <div class="row">
                <div class="col-md-6 text-end ms-auto">
                  <MaterialButton
                    variant="gradient"
                    color="success"
                    type="submit"
                    class="mb-0"
                    >SUBMIT</MaterialButton
                  >
                </div>
              </div>
          </div>
        </div>
      </div>
    </form>
  </div>
</template>