<template>
  <div id="Tabbar">
    <span v-for="item in tabbar">
      <Tabbar-item
        :name="item.tabbar_name"
        :icon="item.tabbar_icon"
        :active="item.tabbar_icon_active"
        :path="item.path"
        :color="active_color" />
    </span>
  </div>
</template>

<script>
import TabbarItem from "./TabbarItem";
export default {
  name: "Tabbar",
  components: {TabbarItem},
  props: {
    tabbar: {
      type: Array,
      default() {
        return []
      }
    },
    active_color: {
      type: String,
      default: 'red'
    }
  }
}
</script>

<style scoped>
@import "../assets/css/tabbar/tabbar.css";
</style>
