<template>
  <table class="table table__custom is-bordered">
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
        <td class="table__item">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
        <td class="table__item table__item_select">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
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
        <td class="table__item">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
        <td class="table__item table__item_select">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
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
        <td class="table__item">-</td>
        <td class="table__item">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
        <td class="table__item table__item_select">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
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
          <p class="table__title">Возможность 4</p>
        </th>
        <td class="table__item">-</td>
        <td class="table__item">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
        <td class="table__item table__item_select">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
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
          <p class="table__title">Возможность 5</p>
        </th>
        <td class="table__item">-</td>
        <td class="table__item">-</td>
        <td class="table__item table__item_select">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
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
          <p class="table__title">Возможность 6</p>
        </th>
        <td class="table__item">-</td>
        <td class="table__item">-</td>
        <td class="table__item table__item_select">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
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
        <td class="table__item">-</td>
        <td class="table__item">-</td>
        <td class="table__item table__item_select">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
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
        <td class="table__item">-</td>
        <td class="table__item">-</td>
        <td class="table__item table__item_select">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
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
          <p class="table__title">Возможность 9</p>
        </th>
        <td class="table__item">-</td>
        <td class="table__item">-</td>
        <td class="table__item table__item_select">-</td>
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
          <p class="table__title">Возможность 10</p>
        </th>
        <td class="table__item">-</td>
        <td class="table__item">-</td>
        <td class="table__item table__item_select">-</td>
        <td class="table__item">
          <img
            class="table__check"
            src="../assets/images/iconCheck.svg"
            alt="есть."
          />
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script>
import InfoPopup from "./InfoPopup.vue";

export default {
  name: "TariffsTable",
  components: { InfoPopup },
  data() {
    return {
      showPopupOne: false,
      showPopupTwo: false,
      showPopupThree: false,
    };
  },
};
</script>

<style>
.table__custom {
  margin-top: 30px;
}

.table__th {
  width: 270px;
  position: relative;
  vertical-align: middle !important;
}

.table__item {
  width: 220px;
  text-align: center !important;
}

.table__item_select {
  background-color: rgba(72, 95, 199, 0.1);
}

.table__check {
  opacity: 0.7;
  width: 25px;
  height: 25px;
}

.table__title {
  font-weight: 500;
}

.table__question {
  width: 20px;
  text-align: center;
  border: 1px solid #000;
  display: block;
  cursor: pointer;
  position: absolute;
  top: 10px;
  right: 10px;
}

@media screen and (max-width: 1224px) {
  .table__th {
    padding: 8px 33px 8px 12px !important;
  }
}

@media screen and (max-width: 432px) {
  .table__th {
    width: 150px;
    padding: 8px 27px 8px 12px !important;
  }

  .table__item {
    width: 30px;
    padding: 2px !important;
    vertical-align: middle !important;
  }

  .table__check {
    width: 20px;
    height: 20px;
    vertical-align: middle;
  }

  .table__question {
    width: 20px;
    top: 7px;
    right: 5px;
  }
}
</style>