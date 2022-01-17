<template>
  <div class="areas-selector grid gap-6 grid-cols-3">
    <template v-if="type=='popular'">
      <a href="#" v-for="area in popularAreas" :key="area.id">
        <figure>
          <img
            class="h-15 mx-auto border rounded shadow-xl"
            :src="area.ensignUrl"
            v-if="area.ensignUrl" />
          <figcaption class="mt-2 text-xs">{{area.name}}</figcaption>
        </figure>
      </a>
    </template>
    <template v-else>
      <a href="#" v-for="area in areas" :key="area.id">
        <figure v-if="area.ensignUrl">
          <img
            class="h-15 mx-auto border rounded shadow-xl"
            :src="area.ensignUrl" />
          <figcaption class="mt-2 text-xs">{{area.name}}</figcaption>
        </figure>
        <figure v-else>
          <img
            class="h-15 mx-auto border rounded shadow-xl"
            src="../assets/No_flag.png" />
          <figcaption class="mt-2 text-xs">{{area.name}}</figcaption>
        </figure>
      </a>
    </template>
  </div>
</template>

<script>
const popularAreas = ['ENG', 'ITA', 'ESP', 'DEU', 'NLD', 'FRA', 'POR'];

export default {
  props: ['type', 'areas'],
  computed: {
    popularAreas() {
      return this.areas.filter((arr) => popularAreas.includes(arr.countryCode));
    },
  },
  mounted() {
    console.log(this.popularAreas);
  },
};
</script>
