<template>
  <div>
     <div id="main" class="studyTime r1" ></div>
    
  </div>
</template>

<script>
import echarts from 'echarts'
export default {
  name: "",
  props: {},
  components: {},
  data() {
    return {
      option: {
           xAxis: {
        type: 'category',
        data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
    },
    yAxis: {
        type: 'value'
    },
    series: [{
        data: [120, 200, 150, 80, 70, 110, 130],
        type: 'bar',
        showBackground: true,
        backgroundStyle: {
            color: 'rgba(220, 220, 220, 0.8)'
        }
    }]
      },
    };
  },
  methods: {
    //实例化图标
    autoMyChart() {
      var myChart = echarts.init(document.getElementById("main"));
      myChart.setOption(this.option);
    },
  },
  mounted() {
    this.autoMyChart()
  },
  watch: {},
  computed: {},
};
</script>

<style lang="scss" scoped>
  .studyTime{
  width: 455rw;
  height: 234rh;
}
</style>