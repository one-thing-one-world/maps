<template>
<div class="container ">
  <div class="top df j-bettween ">
    <div class="imgBox">
      <img v-if="flag === 1" src="../../assets/participantsOnline/head1.png" />
      <img v-if="flag === 2" src="../../assets/participantsOnline/head2.png" />
      <img v-if="flag === 3" src="../../assets/participantsOnline/head3.png" />
    </div>
    <div class="back">返回</div>
    <div class="title ccc">党校可视化场景</div>
    <div class="r1 df">
      <div class="pcApp">综合数据</div>
      <div class="pcApp">PC端</div>
      <div class="pcApp">APP端</div>
    </div>
  </div>

  <div class="content b1">
    <div class="left r1">

      <div class="studyTime r1">
        <studyTime></studyTime>
      </div>
      
      <div class="courseNumber r1">
        <courseNumber></courseNumber>
      </div>

      <div class="userAgeAnalysis r1">
        <userAgeAnalysis></userAgeAnalysis>
      </div>

      <div class="userGenderAnalysis r1">
        <userGenderAnalysis></userGenderAnalysis>
      </div>

    </div>
    <div class="center"></div>
    <div class="right"></div>
  </div>
  
</div>
</template>

<script>
import studyTime from "../../components/participantsOnline/studyTime";
import courseNumber from "../../components/participantsOnline/courseNumber";
import userAgeAnalysis from "../../components/participantsOnline/userAgeAnalysis";
import userGenderAnalysis from "../../components/participantsOnline/userGenderAnalysis";
export default {
  name: "participantsOnline",
  props: {},
  components: {
    studyTime,
    courseNumber,
    userAgeAnalysis,
    userGenderAnalysis,
  },
  data() {
    return {
      flag: 1,
    };
  },
  methods: {},
  mounted() {},
  watch: {},
  computed: {},
};
</script>

<style lang="scss" scoped>



.r1 {
  border: 1px solid red;
}

.top {
  
  width: 100vw;
  height: 90rh;
  position: relative;

  .back {
    margin-left: 40rw;
  }

  .title {
    height: 90rh;
    color: #50e3c2;
    font-size: 36px;
    font-family: PingFangSC-Semibold;
  }

  .imgBox {
    width: 100%;
    height: 90rh;
    position: absolute;
    z-index: -1;

    img {
      width: 100%;
      height: 100%;
    }
  }

  .pcApp {
    margin-right: 1vw;
  }
}

.studyTime {
  width: 455rw;
  height: 234rh;
}

.courseNumber {
  // width: vw(455);
  width: 455rw;
  height: 233rh;
}

.userAgeAnalysis {
  width: 455rw;
  height: 300rh;
}

.userGenderAnalysis {
  width: 455rw;
  height: 178rh;
}
</style>
