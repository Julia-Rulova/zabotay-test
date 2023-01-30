<template>
  <tbody>
    <tr>
      <th class="table__th">
        <p class="table__title">Возможность 1</p>
      </th>
      <td class="table__item">
        <img
          class="table__check"
          src="../assets/images/iconCheck.svg"
          alt="есть."
        />
      </td>
    </tr>
    <tr>
      <th class="table__th">
        <p class="table__title">Возможность 2</p>
      </th>
      <td class="table__item">
        <img
          class="table__check"
          src="../assets/images/iconCheck.svg"
          alt="есть."
        />
      </td>
    </tr>
    <tr>
      <th class="table__th">
        <p class="table__title">Возможность 3</p>
        <span
          class="table__question"
          @mouseover="showPopupOne = true"
          @mouseleave="showPopupOne = false"
        >
          <info-popup
            id="one"
            :showPopup="showPopupOne"
            :popupText="'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'"
          />
          ?</span
        >
      </th>
      <td class="table__item">
        <img
          class="table__check"
          src="../assets/images/iconCheck.svg"
          alt="есть."
          v-if="
            tableType === 'organization' ||
            tableType === 'premium' ||
            tableType === 'pro'
          "
        />
        <p v-else>-</p>
      </td>
    </tr>
    <tr>
      <th class="table__th">
        <p class="table__title">Возможность 4</p>
      </th>
      <td class="table__item">
        <img
          class="table__check"
          src="../assets/images/iconCheck.svg"
          alt="есть."
          v-if="
            tableType === 'organization' ||
            tableType === 'premium' ||
            tableType === 'pro'
          "
        />
        <p v-else>-</p>
      </td>
    </tr>
    <tr>
      <th class="table__th">
        <p class="table__title">Возможность 5</p>
      </th>
      <td class="table__item">
        <img
          class="table__check"
          src="../assets/images/iconCheck.svg"
          alt="есть."
          v-if="tableType === 'organization' || tableType === 'premium'"
        />
        <p v-else>-</p>
      </td>
    </tr>
    <tr>
      <th class="table__th">
        <p class="table__title">Возможность 6</p>
      </th>
      <td class="table__item">
        <img
          class="table__check"
          src="../assets/images/iconCheck.svg"
          alt="есть."
          v-if="tableType === 'organization' || tableType === 'premium'"
        />
        <p v-else>-</p>
      </td>
    </tr>
    <tr>
      <th class="table__th">
        <p class="table__title">Возможность 7</p>
        <span
          class="table__question"
          @mouseover="showPopupTwo = true"
          @mouseleave="showPopupTwo = false"
        >
          <info-popup
            :showPopup="showPopupTwo"
            :popupText="'Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'"
          />
          ?</span
        >
      </th>
      <td class="table__item">
        <img
          class="table__check"
          src="../assets/images/iconCheck.svg"
          alt="есть."
          v-if="tableType === 'organization' || tableType === 'premium'"
        />
        <p v-else>-</p>
      </td>
    </tr>
    <tr>
      <th class="table__th">
        <p class="table__title">Возможность 8</p>
        <span
          class="table__question"
          @mouseover="showPopupThree = true"
          @mouseleave="showPopupThree = false"
        >
          <info-popup
            :showPopup="showPopupThree"
            :popupText="'Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'"
          />
          ?</span
        >
      </th>
      <td class="table__item">
        <img
          class="table__check"
          src="../assets/images/iconCheck.svg"
          alt="есть."
          v-if="tableType === 'organization' || tableType === 'premium'"
        />
        <p v-else>-</p>
      </td>
    </tr>
    <tr>
      <th class="table__th">
        <p class="table__title">Возможность 9</p>
      </th>
      <td class="table__item">
        <img
          class="table__check"
          src="../assets/images/iconCheck.svg"
          alt="есть."
          v-if="tableType === 'organization'"
        />
        <p v-else>-</p>
      </td>
    </tr>
    <tr>
      <th class="table__th">
        <p class="table__title">Возможность 10</p>
      </th>
      <td class="table__item">
        <img
          class="table__check"
          src="../assets/images/iconCheck.svg"
          alt="есть."
          v-if="tableType === 'organization'"
        />
        <p v-else>-</p>
      </td>
    </tr>
  </tbody>
</template>

<script>
import InfoPopup from "./InfoPopup.vue";

export default {
  name: "CardTable",
  components: { InfoPopup },
  data() {
    return {
      showPopupOne: false,
      showPopupTwo: false,
      showPopupThree: false,
    };
  },
  props: {
    tableType: String,
  },
};
</script>

<style>
</style>