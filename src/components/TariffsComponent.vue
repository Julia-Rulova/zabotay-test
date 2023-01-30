<template>
  <section
    class="
      tariffs
      is-flex
      is-flex-direction-row
      is-align-items-center
      is-justify-content-center
    "
    :class="{ 'is-flex-direction-column': width < 1224 }"
  >
    <h1 class="tariffs__title">Получи больше от нашего сайта!</h1>

    <ul
      class="tariffs__list is-flex is-flex-direction-row is-align-items-center"
      :class="{ 'is-flex-direction-column': width < 1224 }"
    >
      <tariff-card
        :title="'Базовый'"
        :price="'Бесплатно'"
        :width="width"
        :showPossibility="showMoreBase"
        @open="showMoreBase = !showMoreBase"
      >
        <card-table :tableType="'base'" />
      </tariff-card>
      <tariff-card
        :title="'Про'"
        :price="'1000'"
        :width="width"
        :showPossibility="showMorePro"
        @open="showMorePro = !showMorePro"
      >
        <card-table :tableType="'pro'"
      /></tariff-card>
      <tariff-card
        :title="'Премиум'"
        :price="'3000'"
        :isActive="true"
        :cardActive="width < 1224 ? true : false"
        :width="width"
        :showPossibility="showMorePremium"
        @open="showMorePremium = !showMorePremium"
      >
        <card-table :tableType="'premium'"
      /></tariff-card>
      <tariff-card
        :title="'Организация'"
        :price="'По запросу'"
        :width="width"
        :showPossibility="showMoreOrganization"
        @open="showMoreOrganization = !showMoreOrganization"
      >
        <card-table :tableType="'organization'"
      /></tariff-card>
    </ul>
  </section>
</template>

<script>
import TariffCard from "./TariffCard.vue";
import CardTable from "./CardTable.vue";

export default {
  name: "tariffs-component",
  components: { TariffCard, CardTable },
  props: {
    width: Number,
  },
  data() {
    return {
      showMoreBase: false,
      showMorePro: false,
      showMorePremium: false,
      showMoreOrganization: false,
    };
  },
};
</script>

<style scoped>
.tariffs {
  width: 100%;
}

.tariffs__title {
  text-align: left;
  margin: 0 20px 0 0;
  font-size: 25px;
  max-width: 250px;
  word-wrap: break-word;
}

@media screen and (max-width: 1224px) {
  .tariffs__title {
    text-align: center;
    margin: 0 0 20px;
  }

  .tariffs__list {
    width: 100%;
  }
}
</style>