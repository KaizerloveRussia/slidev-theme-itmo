<template>
  <div class="ThreeIllustrations">
    <div class="background" :style="{ backgroundImage: `url('./images/ThreeIllustrationsBackground.png')` }"></div>
    <header class="header">
      <slot name="header" />
    </header>
    <div class="content grid grid-cols-3 gap-4">
      <div v-for="i in 3" :key="i" class="set">
        <label :for="'imageInput-' + i" class="image-label">
          <div class="icon-circle">
            <svg viewBox="0 0 24 24" fill="none" stroke="gray" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="feather feather-image"><rect x="3" y="3" width="18" height="18" rx="2" ry="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
          </div>
        </label>
        <input :id="'imageInput-' + i" type="file" accept="image/*" class="image-input" />
        <div class="bold-text">
          <slot :name="`boldText-${i}`" />
        </div>
        <div class="regular-text">
          <slot :name="`regularText-${i}`" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.custom-layout {
  position: relative;
  display: flex;
  flex-direction: column;
  height: 60vh;
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
  z-index: -1;
}

.header {
  font-size: 1.94rem;
  text-align: left;
  margin-bottom: 1rem;
  padding: 0.5rem;
  z-index: 2; 
  color: black;
  position: absolute; 
  top: 6.5%; 
  left: 5.18%;
  font-family: Golos;
  font-weight: bold;
}

.content {
  margin-top: 10%;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  z-index: 1;
  width: 92%;
  margin-left: 3.5%;
}

.set {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1rem;
  width: 100%;
  height: 100%;
}

.image-label {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 6vh;
  background-color: #ccc;
  cursor: pointer;
  user-select: none;
  border-radius: 2vh;
  margin-bottom: 1rem;
  width: 100%;
  height: 60%;
}

.icon-circle {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 23%;
  height: 50%;
  background-color: white;
  border-radius: 50%;
  box-shadow: 0 0.5vh 1vh rgba(0, 0, 0, 0.2);
}

.icon-circle svg {
  width: 50%;
  height: 100%;
}

.image-input {
  display: none;
}

.bold-text {
  color: black;
  font-weight: bold;
  text-align: left;
  margin-bottom: 1rem;
  width: 100%;
  padding: 0.3rem;
  height: 4vh;
  overflow: hidden;
  color: #696969;
  font-family: 'Arial';
}

.regular-text {
  color: black;
  text-align: left;
  width: 100%;
  padding: 0.3rem;
  height: 13.5vh;
  color: gray;
  font-family: 'Arial';

  overflow: hidden;
}
</style>