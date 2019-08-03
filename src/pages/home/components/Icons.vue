<template>
<div class="icons" :options = "swiperOptions">
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
                swiperOptions:{
                    autoplay:false
                    }
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
    },
        props:{
            iconList:Array
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