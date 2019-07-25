<template>
<div class="icons">
    <div class="icon">
        <div class="icon-image">
        <img class="icon-image-content" src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png">
        </div>
        <div class="icon-desc">热门景点</div>
    </div>
        <div class="icon">
        <div class="icon-image">
        <img class="icon-image-content" src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png">
        </div>
        <div class="icon-desc">热门景点</div>
    </div>

      

</div>
    
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
.icons{
    overflow: hidden;
    height:0;
    padding-bottom:50%;
   
    //这样写， 宽高比为2
}
.icon{
    position:relative;
    overflow: hidden;
    height: 0;
    width:25%;
    float:left;
    padding-bottom: 25%;
 
}
.icon-image{
    position: absolute;
    top:0;
    left:0;
    right:0;
    bottom: .44rem;
    
    box-sizing: border-box;
    padding: .1rem;

}
.icon-image-content{
    height: 100%;
    display: block;
    margin: auto;
}
.icon-desc{
    position: absolute;
    bottom:0;
    left:0;
    right:0;
    height: .44rem;
    line-height: .44rem;
    color: #333;
    text-align: center;

}
</style>