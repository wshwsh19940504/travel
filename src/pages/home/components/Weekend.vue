<template>
    <div>
    <div class="recommend-title">周末去哪儿</div>
    <div>
        <div class="item border-bottom" v-for="item of weekendList" :key="item.id">
            <div class="item-img-wrapper">
                <img  class="item-img" :src="item.imgUrl" alt="">
            </div>
            <div class="icon-info">
               <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
           
            </div>
        </div>
    </div>
    </div>
</template>

<script>
    export default {
        name:'HomeWeekend',
        data () {
           return{
           }
        },
    props:{
        weekendList:Array
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
.item-img-wrapper{
overflow: hidden;
height: 0;
padding-bottom: 35%;
// width: 100%;
}
.item-img{
    width:100%;
    // height: 1.7rem;
    // padding: .1rem;
}
.icon-info{
  
   padding: .18rem .2rem .4rem .2rem;
  
}
.item-title{
    line-height: .42rem;
    font-size: .28rem;
   

     overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}
.item-desc{
    line-height: .42rem;
    color: #616161;

 font-size: .24em;
     overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}


</style>