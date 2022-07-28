<template>
  <div class="iframeBox">
    <!-- <div v-for="item,index in arr.result" :key="index">
      <img :style="{height:'300px'}"  :src="item.filePath" alt="">
    </div>  -->
    <div>{{ obj.name }}</div>
    <button @click="del">删除</button>
    <el-input v-model="input" placeholder="请输入内容"></el-input>
    <el-input v-model="input" placeholder="请输入内容"></el-input>
    <el-input v-model="input" placeholder="请输入内容"></el-input>
    <el-input v-model="input" placeholder="请输入内容"></el-input>
    <el-date-picker v-model="value1" type="date" placeholder="选择日期">
    </el-date-picker>
    <el-date-picker v-model="value1" type="date" placeholder="选择日期">
    </el-date-picker>
    <el-input v-model="input" placeholder="请输入内容"></el-input>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {}, 
    };
  },
  beforeCreate() {},
  created() {},

  mounted() {
    this.obj.name = "张三";
    console.log(this.obj);
  },
  methods: {
    del() {
      console.log(this.obj);
      this.$delete(this.obj.target, "name");
      console.log(this.obj.target);
    },
  },
};
</script>

<style lang="less" scoped>
.iframeBox {
  width: 100%;
  height: 100%;
  iframe {
    width: 100%;
    height: 100%;
  }
}
</style>> 