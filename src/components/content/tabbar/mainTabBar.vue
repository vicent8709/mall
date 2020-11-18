<template>
<div>
  <tab-bar>
    <tab-bar-item path="/home">
      <img slot="tab-bar-item-icon" src="~assets/img/tabBar/home.svg"/>
      <img slot="tab-bar-item-icon-active" src="~assets/img/tabBar/home_active.svg"/>
      <div slot="tab-bar-item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category">
      <img slot="tab-bar-item-icon" src="~assets/img/tabBar/category.svg"/>
      <img slot="tab-bar-item-icon-active" src="~assets/img/tabBar/category_active.svg"/>
      <div slot="tab-bar-item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart">
      <img slot="tab-bar-item-icon" src="~assets/img/tabBar/shopcart.svg"/>
      <img slot="tab-bar-item-icon-active" src="~assets/img/tabBar/shopcart_active.svg"/>
      <div slot="tab-bar-item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile">
      <img slot="tab-bar-item-icon" src="~assets/img/tabBar/profile.svg"/>
      <img slot="tab-bar-item-icon-active" src="~assets/img/tabBar/profile_active.svg"/>
      <div slot="tab-bar-item-text">我的</div>
    </tab-bar-item>
  </tab-bar>
</div>
</template>

<script>
import tabBar from "components/tabBar/TabBar";
import tabBarItem from "components/tabBar/TabBarItem"

export default {
  name: "mainTabBar",
  components:{
    tabBar,
    tabBarItem
  }
}
</script>

<style scoped>

</style>
