<template>
  <div class="OnlyText">
    <div class="background" :style="{ backgroundImage: `url('./images/OnlyTextBackground.png')` }"></div>
    <header class="header">
      <slot name="header" />
    </header>
    <div class="field-1">
      <slot name="field1" />
    </div>
  </div>
</template>

<style scoped>
.two-fields-layout {
  position: relative;
  display: flex;
  flex-direction: column;
  height: 57.3vh;
  justify-content: flex-start;
  align-items: center;
}

.background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
}

.header {
  font-size: 1.94rem;
  text-align: left;
  margin-bottom: 1rem;
  z-index: 2;
  color: black;
  position: absolute;
  top: 8%;
  left: 6%;
  font-family: Golos;
  font-weight: bold;
}

.field-1 {
  padding: 0.5rem;
  text-align: left;
  z-index: 1;
  color: black;
  position: absolute;
  top: 24.5%;
  left: 6%;
  width: 81%;
  height: 63%;
  color: gray;
  font-family: 'Arial';

  overflow: hidden; /* Скрытие лишнего текста */
}
</style>