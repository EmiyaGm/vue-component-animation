<template>
  <div class="w-[32px] h-[32px] relative">
    <div
      class="flex items-center justify-center text-base rounded-[50%] bg-[#B5FA44] w-[32px] h-[32px] disappear-bubble text-[#202024] absolute"
    >
      +1
    </div>
  </div>
</template>

<style scoped>
.disappear-bubble {
  -webkit-animation: bubbleDisappear 2s ease-in-out infinite;
  animation: bubbleDisappear 2s ease-in-out infinite;
}

@keyframes bubbleDisappear {
  0% {
    opacity: 1;
    transform: scale(1);
    top: 0;
    left: 0;
  }

  to {
    opacity: 0;
    transform: scale(0);
    top: -40px;
    left: 40px;
  }
}
</style>
