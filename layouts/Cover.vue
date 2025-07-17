<template>
  <div class="Cover">
    <div class="background"></div>
    <div class="content">
      <slot />
    </div>
  </div>
</template>

<style scoped>
@font-face {
  font-family: 'Golos'; 
  src: local('Golos'), url('./fonts/Golos-Text_Regular.ttf');
  font-weight: normal; 
  font-style: normal;
}

@font-face {
  font-family: 'Horizon'; 
  src: local('Horizon'), url('./fonts/ALSGorizont-RegularExpanded.otf'); 
  font-weight: normal; 
  font-style: normal;
}

.custom-background-layout {
  position: relative;
  height: 60vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  z-index: -1;
  background-color: white;
  background-image: none;
}

.content {
  z-index: 1;
  margin-top: 25%;
  text-align: center;
  color: white; 
  font-size: 3rem;
  line-height: 1.5;
  font-family: Golos;
  font-weight: bold;
  color: black;
}
</style>