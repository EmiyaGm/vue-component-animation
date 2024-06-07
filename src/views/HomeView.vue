<script setup lang="ts">
import GradientArrow from '@/components/GradientArrow.vue'
import HaloPoint from '@/components/HaloPoint.vue'
import DisappearBubble from '@/components/DisappearBubble.vue'
import CircleLoading from '@/components/CircleLoading.vue'
</script>

<template>
  <main class="max-w-[1440px] my-0 mx-auto text-center">
    <h1 class="text-3xl font-bold pt-7">页面特效汇总</h1>
    <h3 class="py-7">1.渐变箭头</h3>
    <div class="py-7 w-full border border-white">
      <GradientArrow></GradientArrow>
    </div>
    <h3 class="py-7">2.扩散光晕点</h3>
    <div class="py-7 w-full border border-white">
      <HaloPoint></HaloPoint>
    </div>
    <h3 class="py-7">3.消失远离的+1</h3>
    <div class="py-7 w-full border border-white flex items-center justify-center">
      <DisappearBubble></DisappearBubble>
    </div>
    <h3 class="py-7">4.旋转拖尾Loading</h3>
    <div class="py-7 w-full border border-white flex items-center justify-center">
      <CircleLoading></CircleLoading>
    </div>
  </main>
</template>
