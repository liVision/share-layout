<template>
  <div class="wrap">
    <div class="example2">我在水平垂直居中</div>
</div>
</template>

<style lang="scss" scoped>
  .wrap {
    background-color: orange;
    position: relative;
    width: 300px;
    height: 300px;
}
.example2 {
    background-color: red;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
</style>