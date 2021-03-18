<template>
  <div>
    <router-view></router-view>
    <Tabbar
      :tabbar="tabbar"
      :active_color="active_color" />
  </div>
</template>

<script>
import Tabbar from '../components/Tabbar'
export default {
  name: "Layout",
  components: {Tabbar},
  data() {
    return {
      tabbar: [
        {
          tabbar_name: '首页',
          path: '/home',
          // tabbar_icon: 'https://b.bdstatic.com/miniapp/assets/docs/home_test.svg',
          // tabbar_icon_active: 'https://b.bdstatic.com/miniapp/assets/docs/home_active_test.svg'
          tabbar_icon: 'home.svg',
          tabbar_icon_active: 'home_active.svg'
        },
        {
          tabbar_name: '分类',
          path: '/category',
          // tabbar_icon: 'https://b.bdstatic.com/miniapp/assets/docs/category_test.svg',
          // tabbar_icon_active: 'https://b.bdstatic.com/miniapp/assets/docs/category_active_test.svg'
          tabbar_icon: 'category.svg',
          tabbar_icon_active: 'category_active.svg'
        },
        {
          tabbar_name: '购物车',
          path: '/cart',
          // tabbar_icon: 'https://b.bdstatic.com/miniapp/assets/docs/shopcart_test.svg',
          // tabbar_icon_active: 'https://b.bdstatic.com/miniapp/assets/docs/shopcart_active_test.svg'
          tabbar_icon: 'shopcart.svg',
          tabbar_icon_active: 'shopcart_active.svg'
        },
        {
          tabbar_name: '我的',
          path: '/profile',
          // tabbar_icon: 'https://b.bdstatic.com/miniapp/assets/docs/home_test.svg',
          // tabbar_icon_active: 'https://b.bdstatic.com/miniapp/assets/docs/profile_active_test.svg'
          tabbar_icon: 'profile.svg',
          tabbar_icon_active: 'profile_active.svg'
        }
      ],
      active_color: 'pink'
    }
  }
}
</script>

<style scoped>
</style>
