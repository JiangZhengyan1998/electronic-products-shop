<template>
  <div class="app">
    <div class="daohanglan">
      <el-row :gutter="12">
        <el-col :span="24">
          <el-card shadow="always" style="height:65px;">
            <div class="logo" style="float:left">Logo</div>
            <div style="float:right">
              <el-avatar icon="el-icon-user-solid" style="position:absolute; right:50px; top:15px;"></el-avatar>
            </div>
          </el-card>
        </el-col>
      </el-row>
    </div>
    <br><br><br>
    <div class="neirong">

      <el-carousel :interval="4000" type="card" height="300px">
        <el-carousel-item v-for="item in 6" :key="item">
          <h3 class="medium">{{ item }}</h3>
        </el-carousel-item>
      </el-carousel>

      <el-tabs :tab-position="tabPosition" style="height: 200px;">
        <el-tab-pane label="类别一">
          <el-col :span="4">
            <el-card shadow="hover">
              <div style="height:200px;">
                鼠标悬浮时显示
              </div>
            </el-card>
          </el-col>
        </el-tab-pane>
        <el-tab-pane label="类别二">
          配置管理
        </el-tab-pane>
        <el-tab-pane label="类别三">
          角色管理
        </el-tab-pane>
        <el-tab-pane label="类别四">
          定时任务补偿
        </el-tab-pane>
      </el-tabs>

      
      
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'shouye',
  data () {
    return {
      msg: '',
      tabPosition: 'left'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
   .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 200px;
    margin: 0;
  }
  
  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }
  
  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
</style>
