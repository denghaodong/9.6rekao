<template>
  <div class="home">
    <div class="header">多加网</div>
    <div class="main">
      <swiper>
        <swiper-slide><img src="../assets/logo.png" alt=""></swiper-slide>
        <swiper-slide><img src="../assets/logo.png" alt=""></swiper-slide>
        <swiper-slide><img src="../assets/logo.png" alt=""></swiper-slide>
      </swiper>
      <div v-for="(item,index) in list" :key="index">{{item.name}}</div>
    </div>
  </div>
</template>

<script>
import axios from "axios"
export default {
  data() {
    return {
      list:[]
    }
  },
  name: "home",
  components: {

  },
  created() {
      axios.get("/list").then(res=>{
          this.list=res.data.data
      })
  },
};
</script>
