<template>
  <div class="All_header">
    <v-touch tag="div" @tap="handleBack()" class="back">
      <i class="iconfont icon-mjiantou-copy"></i>
    </v-touch>
    <div class="h-search" id="hSearch">
      <i class="iconfont icon-sousuo"></i>
      <router-link tag="input" to="/searchhouse" type="search" placeholder="搜索新房楼盘或地址"/>
    </div>
    <div class="map">
      <p>地图找房</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ChildHeader",
  methods:{
    handleBack(){
      this.$router.go(-1);
    }
  }
};
</script>

<style lang="scss" scoped>
.All_header {
  width: 100%;
  height: 0.46rem;
  z-index: 102;
  top: 0px;
  left: 0px;
  background-color: #62ab00;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 0.1rem;
   .back{
    height: 0.3rem;
    width: 0.2rem;
    font-size: 0.18rem;
    color: #fff;
  }
}
.h-search {
    height: 0.3rem;
    width: 2rem;
    background-color: #fff;
    opacity: 0.9;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 0.04rem;
    color: #999;
    font-size: 0.14rem;
    padding-left: 0.12rem;
}
.map {
  height: 0.3rem;
  margin-left: 0.05rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-size: 0.15rem;
  color: #fff;
}
</style>