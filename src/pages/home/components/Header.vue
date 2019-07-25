<!--  -->
<template>

  <div class="header">
      <div class="header-left">
        <div class="iconfont back-icon">&#xe7eb;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe63c;</span>
        输入城市/景点/游玩主题</div>
      <div class="header-right">城市
        <span class="iconfont arrow-icon">&#xe615;</span>
      </div>
  </div>

</template>

<script>
  export default {
    data () {
    return {
    }; 
  }
  }
</script>
<style lang='scss' scoped>
@import '../../../assets/styles/varibles.scss';
.header{
  display: flex;
  line-height: .86rem;
  background-color:$bgColor;
  color:#fff;
}
.header-left{
  width: .64rem;
  float: left;
}
.header-input{
  flex:1;
  margin-top: .12rem;
  background: #fff;
  border-radius: .1rem;
  height: .64rem;
  margin-left: .2rem;
  color:#ccc;
  line-height:.64rem;
  padding-left: .2rem;
}
.header-right{
  width: 1.24rem;
  float: right;
  text-align: center;
}
.back-icon{
  text-align: center;
  font-size: .4rem;
}
.arrow-icon{
  font-size: .24rem;
  margin-left:- .04rem;
}
</style>