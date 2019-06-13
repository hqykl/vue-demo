<template>
  <div class="container">
    <div class="answer-num">
      <p class="answer-num-text">题目{{ itemNum }}</p>
    </div>
    <div class="content">
      <div class="awser-block">
        <h6 class="title">{{getAnswer[itemNum-1].topic_name }}</h6>
        <ol class="answer-list">
          <li v-for="(item,index) in getAnswer[itemNum-1].topic_answer" :key="item.topic_id">
            {{ index }}
            {{ item.answer_name }}
          </li>
        </ol>
      </div>
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
      width: 626px;
      height: 600px;
      background: url('../assets/2-1.png') no-repeat;
      background-size: 626px auto;
      color: #eee;
      text-align: left;
    }
    .title {
      margin: 0;
      font-size: 32px;
      font-weight: 400;
    }
    .awser-block {
      position: absolute;
      left: 50%;
      top: 50px;
      transform: translateX(-50%);
      width: 400px;
    }
    .answer-list {
      padding: 0;
      list-style: none;
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