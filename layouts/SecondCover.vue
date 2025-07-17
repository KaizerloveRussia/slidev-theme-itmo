<template>
  <div class="SecondCover">
    <div class="background"></div>
    <div class="content">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.custom-background-layout {
  position: relative;
  height: 60vh;
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.background {
  z-index: -1;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: right;
  background-image: none;
  background-color: white;
}

.content {
  margin-top: 25%;
  z-index: 1;
  text-align: left; 
  color: white; 
  font-size: 2.69rem;
  line-height: 1.5;
  padding-left: 2rem;
  font-family: Golos;
  font-weight: bold;
  color: black;
}
</style>