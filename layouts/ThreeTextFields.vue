<template>
  <div class="ThreeTextFields">
    <div class="background" :style="{ backgroundImage: `url('./images/ThreeTextFieldsBackground.png')` }"></div>
    <header class="header">
      <slot name="header" />
    </header>
    <div class="grid grid-cols-2 gap-4 fields-grid">
      <div class="col-span-1 row-span-1 field-1">
        <slot name="field1" />
      </div>
      <div class="col-span-1 row-span-2 field-3">
        <slot name="field3" />
      </div>
      <div class="col-span-1 row-span-1 field-2">
        <slot name="field2" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.three-fields-layout {
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

.fields-grid {
  margin-top: 10.8%;
  margin-left: 4.8%;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: minmax(30%, auto) minmax(30%, auto);
  gap: 1vh;
  position: relative;
}

.field-1 {
  grid-column: 1;
  grid-row: 1;
  padding: 0.5rem;
  text-align: left;
  z-index: 1;
  color: black;
  width: 94%;
  height: 49%;
  color: white;
  font-family: 'Arial';

  overflow: hidden;
}

.field-2 {
  grid-column: 1;
  grid-row: 2;
  padding: 0.5rem;
  text-align: left;
  z-index: 1;
  color: black;
  width: 94%;
  margin-top: -43%;
  height: 98%;
  color: white;
  font-family: 'Arial';
  
  overflow: hidden;
}

.field-3 {
  grid-column: 2;
  grid-row: 1 / span 2;
  padding: 0.5rem;
  text-align: left;
  z-index: 1;
  color: black;
  margin-left: -3%;
  width: 84%;
  height: 65%;
  color: white;
  font-family: 'Arial';

  overflow: hidden;
}
</style>