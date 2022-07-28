<template>
  <div id="main"></div>
</template>

<script> 

export default {
  name: "Home",
  components: {},
  methods: {
    initEarth() {
      var echarts = require("echarts");
      require("echarts-gl");

      var ROOT_PATH =
        "https://cdn.jsdelivr.net/gh/apache/echarts-website@asf-site/examples";

      var chartDom = document.getElementById("main");
      var myChart = echarts.init(chartDom);
      var option;

      option = {
        backgroundColor: "#000",
        globe: {
          // baseTexture: ROOT_PATH + "/data-gl/asset/earth.jpg",
          baseTexture: require('../assets/img/result_bg.jpg'),
          shading: "lambert",
          // environment: ROOT_PATH + "/data-gl/asset/starfield.jpg",
          environment: require('../assets/img/result_bg.jpg'),
          atmosphere: {
            show: true,
          },
          light: {
            ambient: {
              intensity: 0.1,
            },
            main: {
              intensity: 1.5,
            },
          },
        },
        series: [],
      };

      option && myChart.setOption(option);
    },
  },
  mounted() {
    this.initEarth()
  },
};
</script>
<style >
 #main{
   height: 100%;
 }
</style>
