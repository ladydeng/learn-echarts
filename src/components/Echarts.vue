<template>
  <div id="Echarts">
    <div id="main" ref="main"></div>
    <p class="text">这是一个段落</p>
  </div>
</template>

<script>
import * as echarts from "echarts";
export default {
  name: "Echarts",
  mounted() {
    // 基于准备好的dom，初始化echarts实例
    var myChart = echarts.init(this.$refs.main);
    // 绘制图表
    myChart.setOption({
      title: {
        text: "ECharts 入门示例",
      },
      tooltip: {},
      xAxis: {
        data: ["衬衫", "羊毛衫", "雪纺衫", "裤子", "高跟鞋", "袜子"],
      },
      yAxis: {},
      series: [
        {
          name: "销量",
          type: "bar",
          data: [5, 20, 36, 10, 10, 20],
        },
        {
          name: "销量",
          type: "line",
          data: [10, 25, 50, 15, 15, 25],
        },
      ],
    });
  },
};
</script>

<style lang="less">
@color:red;
#main {
  width: 50vw;
  height: 500px;
}

.text{
    color:@color
}
</style>
