<template>
  <div class="loading-view"></div>
</template>

<style scoped>
/* 定义一个名为loading的关键帧动画，用于旋转360度 */
@-webkit-keyframes loading {
  /* 0% 动画开始 */
  0% {
    -webkit-transform: rotate(0deg);
  }
  /* 100% 动画结束 */
  100% {
    -webkit-transform: rotate(360deg);
  }
}
@keyframes loading {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
/* 定义loading-view类，设置大小、形状、背景、位置和动画 */
.loading-view {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  position: relative;
  /* 创建一个从透明到蓝色的渐变效果，圆锥渐变（颜色过渡围绕中心点旋转） */
  background: conic-gradient(rgba(181, 250, 68, 0) 0%, #b5fa44 100%);
  /* 设置动画时间为1.5s，并使其无限循环 */
  animation: loading ease-in-out 1.5s infinite;
}
/* 定义loading-view的伪元素::after，设置大小、形状、背景、位置 */
/* ::after用于创建一个小的蓝色圆形 */
.loading-view::after {
  position: absolute;
  width: 1px;
  height: 1px;
  background: #b5fa44;
  border-radius: 50%;
  content: '';
  left: 50%;
  transform: translateX(-50%);
}
/* 定义loading-view的伪元素::before，设置大小、形状、背景、位置 */
/* ::before用于创建一个大的白色圆形。这两个伪元素与.loading-view类一起旋转，从而形成旋转loading的效果 */
.loading-view::before {
  content: '';
  width: 100%;
  height: 100%;
  border-radius: 50%;
  background-color: black;
  transform: scale(0.98);
  position: absolute;
  top: 0;
  left: 0;
}
</style>
