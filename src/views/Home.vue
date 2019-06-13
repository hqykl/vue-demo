<template>
  <div class="home">
    <div class="answer-num">
      <p class="answer-num-text">第一周</p>
    </div>
    <div class="content"></div>
    <router-link to="/about" class="button"></router-link>
  </div>
</template>

<style lang="scss" scoped>
  .home {
    position: relative;
    height: 1334px;
    width: 100%;
    background: url('../assets/1-1.jpg') no-repeat center;
    background-size: auto 1334px;
    .answer-num {
      position: absolute;
      top: 0;
      right: 80px;
      width: 148px;
      height: 296px;
      background: url('../assets/WechatIMG2.png') no-repeat;
      background-size: 148px auto;
    }
    .answer-num-text {
      position: absolute;
      bottom: 10px;
      left: 0;
      width: 100%;
      font-size: 26px;
    }
    .content {
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
      top: 20%;
      width: 526px;
      height: 465px;
      background: url('../assets/1-2.png') no-repeat;
      background-size: 526px auto;
    }
    .button {
      position: absolute;
      transform: translateX(-50%);
      bottom: 400px;
      left: 50%;
      width: 173px;
      height: 84px;
      background: url('../assets/1-4.png') no-repeat;
      background-size: 173px auto;
    }
  }
</style>

