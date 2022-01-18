<template>
  <section class="home">
    <div>
      <div class="flex mb-4 justify-between items-center">
      <h2 class="text-left text-3xl">Popular Areas</h2>
      <router-link to="/all-areas" class="inline-block py-1 px-3 underline underline-offset-4">
        <span class="text-xs">
          See All
        </span>
      </router-link>
      </div>
      <areas-selector :areas="areas" type="popular"/>
    </div>

    <div class="mt-24">
    <h2 class="h1 text-left text-3xl mb-3">Popular Competition</h2>
    </div>
  </section>
</template>

<script>
import AreasSelector from '@/components/AreasSelector.vue';
import axios from 'axios';

const AREAS_DATA = require('../../data/areas.json');

export default {
  name: 'Home',
  data() {
    return {
      areas: AREAS_DATA.areas,
    };
  },
  components: {
    AreasSelector,
  },
  methods: {},
  mounted() {
    const url = 'https://api.football-data.org/v2/areas/';

    axios
      .get(
        url,
        {
          headers: {
            'X-Auth-Token': '7880b2049a8d4c829f28937beabc0d76',
          },
        },
      )
      .then(
        (response) => console.log(response),
      );
  },
};
</script>
