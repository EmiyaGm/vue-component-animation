<template>
  <span class="title text-base">这里是标题</span>
</template>

<style scoped>
.title {
  color: rgba(255, 255, 255, 0.47) !important;
  transition: 0.3s !important;
  position: relative;
  text-decoration: none !important;
  -webkit-transition: color 0.4s ease-out !important;
  transition: color 0.4s ease-out !important;
}
.title::after {
  border-top: 0.5px solid #fff;
  bottom: 0px;
  content: '';
  left: 0;
  position: absolute;
  right: 100%;
  -webkit-transition: border-color 0.4s ease-out;
  transition: border-color 0.4s ease-out;
}
.title:hover::after {
  animation: anchor-underline 2s cubic-bezier(0, 0.5, 0, 1) infinite;
  border-color: #fff;
}
@keyframes anchor-underline {
  0%,
  10% {
    left: 0;
    right: 100%;
  }
  40%,
  60% {
    left: 0;
    right: 0;
  }
  90%,
  100% {
    left: 100%;
    right: 0;
  }
}
</style>
