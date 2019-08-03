<!--  -->
<template>

  <div>
   <home-header :city='city'></home-header>
   <home-swiper :List='swiperList'></home-swiper>
   <home-icons :iconList = 'iconList'></home-icons>
   <home-recommend :recommendList = 'recommendList'></home-recommend>
   <home-weekend :weekendList = 'weekendList'></home-weekend>
  </div>

</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from  './components/Icons'
import HomeRecommend from  './components/Recommend'
import HomeWeekend from  './components/Weekend'
// import axios from 'axios'
// import { log } from 'util';
// const newLocal=axios.get('/api');
export default {
  data() {
    return {
      city:'',
      swiperList:[],
      recommendList:[],
      iconList:[],
      weekendList:[]
    }
  },
  components:{
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
//  created() {
//     axios.get('https://www.easy-mock.com/mock/5d42f3a617d61260a34e33a1/mock/mock1').then(res => {console.log(res)})

//   }
  methods:{
    getHomeInfo(){
      this.$http.get('/api/banner')
      .then(this.getHomeInfoSucc)
    },
  getHomeInfoSucc(res){
    res = res.data
    if (res.data) {
      const data = res.data
      this.city = data.city
      this.swiperList = data.swiperList
      this.recommendList = data.recommendList
      this.iconList = data.iconList
      this.weekendList = data.weekendList
      console.log(this.city)
    }
   console.log(res)
  }

  },
  mounted() {
    this.getHomeInfo()
  },
}

</script>
<style lang='scss' scoped>

</style>