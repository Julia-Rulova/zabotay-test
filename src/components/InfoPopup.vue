<template>
  <Transition name="popup">
    <div v-if="showPopup" class="popup">
      <p class="popup__text">
        {{ popupText }}
      </p>
      <div class="popup__arrow" />
    </div>
  </Transition>
</template>

<script>
export default {
  name: "infoPopup",
  props: {
    popupText: String,
    showPopup: Boolean,
  },
};
</script>

<style scoped>
.popup {
  background-color: #fff;
  box-shadow: 0px 10px 36px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  position: absolute;
  bottom: 33px;
  right: -5px;
  width: 200px;
}

.popup__text {
  font-style: normal;
  font-weight: 400;
  font-size: 13px;
  line-height: 1.4;
  text-align: center;
  letter-spacing: -0.4px;
  color: #000;
  margin: 7px 11px;
}

.popup__arrow {
  background-color: #fff;
  width: 9px;
  height: 9px;
  transform: rotate(45deg);
  position: absolute;
  bottom: -3px;
  right: 12px;
  border-radius: 2px;
}

.popup-enter-active,
.popup-leave-active {
  transition: transform 0.5s ease;
}

.popup-enter-from,
.popup-leave-to {
  transform: translateY(-30px);
  transition: transform 0.5s ease;
}
</style>