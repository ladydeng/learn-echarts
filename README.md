## 在vue中使用echarts
   1.安装命令：npm install echarts --save
   2.使用：直接在vue文件中导入import * as echarts from "echarts"就可以使用了;
   3.或者按需导入:
      // 引入 echarts 核心模块，核心模块提供了 echarts 使用必须要的接口。
       import * as echarts from 'echarts/core';
       // 引入柱状图图表，图表后缀都为 Chart
       import {
           BarChart
       } from 'echarts/charts';
## 在vue中使用less
   1.安装命令：npm install --save less less-loader
   2.配置：

   3.使用：<style lang="less"></style>
   配置到这里使用的话可能报错：Syntax Error: TypeError: this.getOptions is not a function
   报错原因：less-loader版本太高
   解决：卸载（npm uninstall --save less-loader）再重新安装一个较低版本(npm i --save less-loader)
