<template>
  <div id="app">
    <div class="block" style="width:1200px">
      <span class="demonstration">历史时间轴</span>
      <el-slider
        v-model="value"
        :show-tooltip="false"
        range
        :marks="marks"
        @change="handleChange">
      </el-slider>
    </div>

    <div class="table">
      <Table1900 v-show="active===1" style="width:1200px"></Table1900>
      <War1  v-show="active===2" style="width:1200px"></War1>
      <War2  v-show="active===3" style="width:1200px"></War2>
      <After  v-show="active===4" style="width:1200px"></After>
      <div class="tuli"> 
        <span>图例：  </span>
        <img src="./assets/friends.png" style="width: 20px;height: 20px">
        Friends 
        <img src="./assets/enemy.png" style="width: 20px;height: 20px">
        Enemy 
        <img src="./assets/complicated.png" style="width: 20px;height: 20px">
        Complicated 
      </div>
    </div>

  </div>
</template>

<script>
import Table1900 from './components/Table1900.vue'
import War2 from './components/War2.vue'
import War1 from './components/War1.vue'
import After from './components/AfterWar2.vue'

export default {
  name: 'App',
  components: {
    // 注册组件
    Table1900,
    War1,
    War2,
    After,
    
  },
  data() {
    return {
      active:3,
      value: [0,30],
      marks: {
        10: '1900八国联军侵华',
        30: '一战',
        60: '二战',
        90: '二战后至今'
      }
    }
  },
  methods: {
    //跳转不同时期的关系图
    handleChange() {
      console.log(this.value[1])
      if(this.value[1]==10){
        console.log("跳转到table")
        this.active=1
      }
      if(this.value[1]==30){
        console.log("跳转到war1")
        this.active=2
      }
      if(this.value[1]==60){
        console.log("跳转到war2")
        this.active=3
      }
      if(this.value[1]==90){
        console.log("跳转到Afterwar2")
        this.active=4
      }
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  /* -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale; */
  /* text-align: center; */
  color: #2c3e50;
  /* margin-top: 60px; */
  margin-left: 30px;
}

.table{
  margin-top: 40px;
}
.tuli{
  font-size: 20px;
  margin-left: 800px;
  margin-top: 30px;
  margin-bottom: 10px;
}
.block{
  font-size: 20px;
  margin-left: 10px;
}
.demonstration{
  text-align: center;
}

</style>
