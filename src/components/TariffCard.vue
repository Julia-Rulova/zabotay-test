<template>
  <article
    class="
      card__custom card
      is-flex
      is-flex-direction-column
      is-justify-content-center
      is-align-items-center
    "
    :class="{ card__active: cardActive }"
  >
    <h2 class="card__title">{{ title }}</h2>
    <p class="card__price">{{ checkPrice }}</p>
    <button class="button is-link card__btn" :class="{ 'is-light': !isActive }">
      Подключить
    </button>

    <div class="card__more" @click="$emit('open')" v-if="width < 1224">
      <p class="card__more-title">Увидеть больше возможностей</p>
      <p
        class="card__more-arrow"
        :class="{ 'card__more-arrow_active': showPossibility }"
      >
        >
      </p>
    </div>

    <table
      class="table table__custom is-bordered"
      v-if="showPossibility && width < 1224"
    >
      <slot></slot>
    </table>
  </article>
</template>

<script>
export default {
  name: "TariffCard",
  props: {
    title: String,
    price: String,
    isActive: Boolean,
    cardActive: Boolean,
    showPossibility: Boolean,
    width: Number,
  },
  computed: {
    checkPrice() {
      return isNaN(Number(this.price)) ? this.price : `${this.price} ₽`;
    },
  },
};
</script>

<style scoped>
.card__custom {
  width: 200px;
  padding: 20px;
  margin-right: 20px;
}

.card__custom:last-of-type {
  margin: 0;
}

.card__title {
  font-size: 20px;
}

.card__price {
  font-size: 22px;
  font-weight: 500;
  margin: 20px 0;
}

.card__active {
  background-color: rgba(72, 95, 199, 0.1);
}

.table__custom {
  background-color: transparent;
  width: 90%;
}

.card__more {
  display: flex;
  flex-direction: row;
  justify-content: center;
  color: #485fc7 !important;
  cursor: pointer;
  border: none !important;
  margin: 20px 0 0;
}

.card__more-title {
  font-weight: 500;
  margin-right: 15px;
}

.card__more-arrow {
  font-size: 20px;
  line-height: 22px;
}

.card__more-arrow_active {
  margin-top: 3px;
  transform: rotate(90deg);
}

@media screen and (max-width: 1224px) {
  .card__custom {
    width: 90%;
    padding: 20px;
    margin-right: 0;
    margin-bottom: 20px;
  }

  .card__custom:last-of-type {
    margin: 0;
  }
}

@media screen and (max-width: 376px) {
  .card__more-title {
    width: 200px;
  }

  .card__more-arrow {
    margin-top: 15px;
  }
}
</style>