<template>
<div class="wrapper">
<van-swipe :autoplay="2000" indicator-color="white">
  <van-swipe-item v-for="(item,index) in List" :key="index">
    <img class="swiper-img" :src="item.imgUrl"/>
    </van-swipe-item>

</van-swipe>
</div> 
</template>

<script>
    export default {
        name:"HomeSwiper",
        data (){
            return{
             
          
           
            }
        },
        props:{
            List:Array
        }
            
        
    // async created() {
    //     try {
         
    //         const items= await this.$http.get('/api/banner')
    //         this.swiperList=items.data
    //         console.log(this.swiperList)
    //     } catch (err) {
    //         console.log(err)
    //     }  
    //   }
    }
</script>

<style lang="scss" scoped>

.swiper-img{
  width:100%;
}

</style>