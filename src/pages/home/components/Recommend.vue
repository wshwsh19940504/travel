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
           return{ recommendList:[{
               id:'0001',
               imgUrl:'http://img1.qunarzz.com/sight/p0/1905/e6/e683c8cf5e97ce03a3.img.jpg_200x200_4769276c.jpg',
               title:'世界之窗',
               desc: '44596评论'
           },{
               id:'0002',
               imgUrl:'http://img1.qunarzz.com/sight/p0/1507/64/34362835b4a219af8b36803d31a6380f.water.jpg_200x200_bc5c0452.jpg',
               title:'深圳小梅沙',
               desc: '44596评论'
           },{
               id:'0003',
               imgUrl:'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_200x200_1c15c8f5.jpg',
               title:'深圳野生动物园',
               desc: '44596评论'
           }

           ]}
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