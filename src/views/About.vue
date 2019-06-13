<template>
  <div class="container">
    <div class="answer-num">
      <p class="answer-num-text">题目{{ itemNum }}</p>
    </div>
  </div>
</template>
<style lang="scss" scoped>
  .container {
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
      // background: url('../assets/1-2.png') no-repeat;
      // background-size: 526px auto;
    }
  }
</style>
<script>
// @ is an alias to /src
import {mapGetters, mapState} from 'vuex'

export default {
  name: 'home',
  components: {
  },
  data() {
    return {

    }
  },
  created() {
    console.log(this.getAnswer)
  },
  computed: {
    ...mapGetters(['getAnswer']),
    ...mapState(['itemNum'])
  }
}
</script>