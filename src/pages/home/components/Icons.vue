<template>
<div class="icons">
      <swiper >
    <swiper-slide v-for="(page,index) of pages" :key="index">
    <div class="icon" v-for="item of page" :key="item.id">
        <div class="icon-image">
        <img class="icon-image-content" :src="item.imgUrl">
        </div>
        <div class="icon-desc">{{item.desc}}</div>
    </div>
    </swiper-slide>


     </swiper>

</div>
    
</template>

<script>
    export default {
        data (){
  return {

        iconList: [{
            id:'0001',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
         desc:'景点门票'
        },
        {
            id:'0002',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
         desc:'深圳必游我在深圳'
        },
        {
            id:'0003',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/4d/a1eda1a2b8414302.png',
         desc:'广州融创'
        },
        {
            id:'0004',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
         desc:'暑期夜场'
        },
        {
            id:'0005',
            imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/bda58ffc3016edad84e656e8a94b0321.png',
         desc:'深圳动物园'
        },
        {
            id:'0006',
            imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/cba147cf6cfcea7109d0bff6aac6f626.png',
         desc:'玩转澳门'
        },
        {
            id:'0007',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/a6/6d97515091789602.png',
         desc:'水上乐园'
        },
        {
            id:'0008',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
         desc:'东部华侨城'
        },
        {
            id:'0009',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
         desc:'世界之窗'
        }
      
      ]
      }
     
        },
    
    computed:{
        pages (){
            const pages= []
            this.iconList.forEach((item,index) =>{
                const page =Math.floor(index/8)
                if(!pages[page]){
                    pages[page]=[]
                }
                pages[page].push(item)
            } )
            return pages
        }
    }
        
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

    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
// 这三行代码可以实现文字内容过多时候，出现...省略号
}
</style>