<template>
  <section class="app is-flex is-flex-direction-column is-align-items-center">
    <tariffs-component :width="width" />

    <tariffs-table v-if="width >= 1224" />
  </section>
</template>

<script>
import TariffsComponent from "./components/TariffsComponent.vue";
import TariffsTable from "./components/TariffsTable.vue";

export default {
  name: "App",
  components: { TariffsComponent, TariffsTable },
  data() {
    return {
      width: window.innerWidth,
    };
  },
  methods: {
    updateWidth() {
      this.width = window.innerWidth;
    },
  },
  created() {
    window.addEventListener("resize", this.updateWidth);
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 40px;
  min-height: 100vh;
}

@media screen and (max-width: 432px) {
  .app {
    padding: 20px 10px;
  }
}
</style>
