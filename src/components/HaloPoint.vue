<template>
  <div className="dot">
    <div className="dot-inner"></div>
  </div>
</template>

<style scoped>
.dot {
  display: inline-block;
  position: relative;
  width: 18px;
  height: 18px;
  background: #b5fa44;
  border-radius: 50%;
  margin-right: 10px;
}

.dot-inner {
  background: #b5fa44;
  position: absolute;
  top: 0;
  left: 0;
  box-sizing: border-box;
  display: block;
  width: 100%;
  height: 100%;
  border-radius: 50%;
  -webkit-animation: vabDot 1.2s ease-in-out infinite;
  animation: vabDot 1.2s ease-in-out infinite;
}

@-webkit-keyframes vabDot {
  0% {
    opacity: 0.6;
    transform: scale(0.8);
  }

  to {
    opacity: 0;
    transform: scale(2.4);
  }
}

@keyframes vabDot {
  0% {
    opacity: 0.6;
    transform: scale(0.8);
  }

  to {
    opacity: 0;
    transform: scale(2.4);
  }
}
</style>
