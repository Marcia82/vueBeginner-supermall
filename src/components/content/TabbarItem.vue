<template>
  <div id="TabbarItem" @click="clickActive">
    <img v-if="!isActive" :src="img(icon)" />
    <img v-else :src="img(active)" />
    <div class="tabbar-name"
      :style="{'color': (isActive ? color: '#000000')}">{{name}}</div>
  </div>
</template>

<script>
export default {
  name: "TabbarItem",
  props: {
    name: {
      type: String,
      default: ''
    },
    path: {
      type: String,
      default: ''
    },
    icon: {
      type: String,
      default: ''
    },
    active: {
      type: String,
      default: ''
    },
    color: {
      type: String,
      default: ''
    }
  },
  computed: {
    isActive() {
      return this.$route.path.indexOf(this.path) !== -1;
    }
  },
  methods: {
    img(item) {
      return require('../assets/img/tabbar/' + item);
    },
    clickActive() {
      this.$router.replace(this.path)
    }
  }
}
</script>

<style scoped>
@import "../assets/css/tabbar/tabbaritem.css";
</style>
