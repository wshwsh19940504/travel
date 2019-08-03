<template>
    <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <div class="item-img-wrapper">
                <img  class="item-img" :src="item.imgUrl" alt="">
            </div>
            <div class="icon-info">
               <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
            </div>
        </li>
    </ul>
    </div>
</template>

<script>
    export default {
        name:'HomeRecommend',
        data () {
           return{
           }
        },
        props:{
            recommendList:Array
        }
    }
</script>

<style lang="scss" scoped>
.recommend-title{
    line-height:.8rem;
    background: #eee;
    text-indent: .2rem;
    margin-top: .2rem;
}
.item{
    display: flex;
    height: 1.9rem;
  
    overflow: hidden;
}
.item-img{
    width: 1.7rem;
    height: 1.7rem;
    padding: .1rem;
}
.item-info{
    flex: 1;
    padding: .1rem;
    min-width:0;
}
.item-title{
    line-height: .54rem;
    font-size: .32rem;
     overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}
.item-desc{
    line-height: .4rem;
    color: #616161;
     overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}

.item-button{
    margin-top: .16rem;
    background: #ff9300;
    padding: 0 .2rem;
    border-radius: .09rem;
    color: #fff;
    line-height: .44rem;
}
</style>