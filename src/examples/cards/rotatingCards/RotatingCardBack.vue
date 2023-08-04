<script setup>
defineProps({
  image: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  description: {
    type: Array,
    required: true,
  },
  action: {
    type: Array,
    route: String,
    label: String,
    color: String,
    required: true,
  },
});
</script>
<template>
  <div
    class="back back-background"
    :style="{
      backgroundImage: `url(${image})`,
      backgroundSize: 'cover',
    }"
  >
    <div class="card-body pt-2 text-center">
      <h3 class="text-white" v-html="title"></h3>    

      <ul class="flex-column ms-n3 nav">
        <!-- Loop through the description array and render each item as a list item -->
        <li v-for="(desc, index) of description" 
        :key="index" class="my-1 pl-4 relative">
    <span class="list-marker absolute left-0 top-1">&#8226;</span>
    {{ desc }}</li>
      </ul>
      <div class="buttons-group">
        <a
          v-for="({ route, color, label }, index) of action"
          :key="index"
          :href="route"
          target="_blank"
          class="btn btn-sm mt-3 inline-block ms-1"
          :class="`${color ? `btn-${color}` : 'btn-white'}`"
          >{{ label }}</a
        >
      </div>
    </div>
  </div>
</template>
