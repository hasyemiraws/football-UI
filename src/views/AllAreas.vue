<template>
  <div class="all-areas">
    <h2 class="text-center text-3xl mb-4">All Areas</h2>
    <form class="group relative mb-4">
      <svg width="20" height="20"
        fill="currentColor"
        class="absolute
            left-3
            top-1/2
            -mt-2.5
            text-slate-400
            pointer-events-none
            group-focus-within:text-blue-500"
        aria-hidden="true">
        <path fill-rule="evenodd"
            clip-rule="evenodd"
            d="M8 4a4 4 0 100 8 4 4 0 000-8zM2
                8a6 6 0 1110.89 3.476l4.817
                4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
        />
      </svg>
      <input class="focus:ring-2 focus:ring-blue-500
        focus:outline-none appearance-none w-full text-sm
        leading-6 text-slate-900 placeholder-slate-400
        rounded-md py-2 pl-10 ring-1 ring-slate-200 shadow-sm"
        type="text" aria-label="Filter areas" placeholder="Filter areas...">
    </form>
    <areas-selector :areas="areas"/>
  </div>
</template>

<script>
import AreasSelector from '@/components/AreasSelector.vue';

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
};
</script>
