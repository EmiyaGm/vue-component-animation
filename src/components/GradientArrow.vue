<template>
  <div>
    <div className="arrows-body">
      <div className="arrow"></div>
      <div className="arrow"></div>
      <div className="arrow"></div>
      <div className="arrow"></div>
    </div>
  </div>
</template>

<style scoped>
.arrows-body {
  display: flex;
  align-items: center;
  justify-content: center;
}

.arrow {
  position: relative;
  width: 13px;
  height: 13px;
  border-bottom: 1px solid white;
  border-right: 1px solid white;
  transform: rotate(-45deg);
  animation: arrow-load 2s infinite;
}

.arrow:nth-child(1) {
  left: 10.5px;
  animation-delay: -0.6s;
}

.arrow:nth-child(2) {
  left: 21px;
  animation-delay: -0.4s;
}

.arrow:nth-child(3) {
  left: 31.5px;
  animation-delay: -0.2s;
}

.arrow:nth-child(4) {
  left: 42px;
}

@keyframes arrow-load {
  0% {
    opacity: 0;
    transform: rotate(-45deg) translate(-13px, -13px);
  }
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: rotate(-45deg) translate(13px, 13px);
  }
}
</style>
