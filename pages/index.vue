<template>
  <div>
    <el-carousel height="700px" class="carousel">
      <el-carousel-item v-for="(item, index) in banners" :key="index">
        <div class="banners" :style="`background:url(${$axios.defaults.baseURL + item.url}) center center no-repeat; `"></div>
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
export default {
  data () {
    return {
      banners: [
        // "http://157.122.54.189:9095/assets/images/th01.jfif",
        // "http://157.122.54.189:9095/assets/images/th02.jfif",
        // "http://157.122.54.189:9095/assets/images/th03.jfif",
        // "http://157.122.54.189:9095/assets/images/th014.jfif"
      ]
    }
  },
  mounted(){
    this.$axios({
      url:"/scenics/banners"
    }).then(res=>{
      // console.log(res)
      const {data} = res.data;
      this.banners = data;
    })
  }
}
</script>

<style lang="less" scoped>
.carousel {
  min-width: 1000px;
}
.banners {
  height: 700px;
}
</style>