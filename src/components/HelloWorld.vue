<template>
  <div class="hello">
    <el-tabs v-model="activeName" @tab-click="tabClick">
      <el-tab-pane label="用户管理" name="1" v-on:click.self="handle">用户管理</el-tab-pane>
      <el-tab-pane label="配置管理" name="2">配置管理</el-tab-pane>
      <el-tab-pane label="角色管理" name="3">角色管理</el-tab-pane>
      <el-tab-pane label="定时任务补偿" name="4">定时任务补偿</el-tab-pane>
    </el-tabs>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeName: "second",
      msg: "Welcome to Your Vue.js App",
      listd: ["用户管理", "配置管理", "角色管理", "定时任务补偿"]
    };
  },
  methods: {
    handle() {
      this.$emit("click", function() {
        alert("123123");
      });
    },
    tabClick(tab, event) {
      console.log(tab.name);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
