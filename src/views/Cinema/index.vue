<template>
  <div id="main" >
    <Header title="喵喵影院"/>
    <div id="content">
      <div class="cinema_menu">
        <router-link to="/cinema/ciList" tag="div" class="city_switch">
          全城<i class="iconfont icon-xiala"></i>
        </router-link>
        <router-link to="/cinema/brand" tag="div" class="brand_switch">
          品牌<i class="iconfont icon-xiala"></i>
        </router-link>
        <router-link to="/cinema/feature" tag="div" class="feature_switch">
          特色<i class="iconfont icon-xiala"></i>
        </router-link>
      </div>
      <keep-alive>
        <router-view/>
      </keep-alive>
    </div>
    <TabBar/> 
  </div>
</template>

<script>
import Header from '@/components/Header'
import TabBar from '@/components/TabBar'
export default {
  name: 'Cinema',
  components: {
    Header,
    TabBar
  }
}
</script>

<style scoped>
  #content .cinema_menu {
    width: 100%;
    height: 45px;
    border-bottom: 1px solid #e6e6e6;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background: white;
    line-height: 45px;
  }
  .cinema_menu .city_switch {
    width: 80px;
    text-align: center;
  } 
  .cinema_menu .city_switch.active {
    color: #ef4238;
    border-bottom: 2px solid #ef4238;
  }
  .cinema_menu .city_switch.router-link-active {
    color: #ef4238;
    border-bottom: 2px solid #ef4238;
  }
  .cinema_menu .brand_switch {
    width: 80px;
    text-align: center;
  } 
  .cinema_menu .brand_switch.active {
    color: #ef4238;
    border-bottom: 2px solid #ef4238;
  }
  .cinema_menu .brand_switch.router-link-active {
    color: #ef4238;
    border-bottom: 2px solid #ef4238;
  }
  .cinema_menu .feature_switch {
    width: 80px;
    text-align: center;
  } 
  .cinema_menu .feature_switch.active {
    color: #ef4238;
    border-bottom: 2px solid #ef4238;
  }
  .cinema_menu .feature_switch.router-link-active {
    color: #ef4238;
    border-bottom: 2px solid #ef4238;
  }

</style>