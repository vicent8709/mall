<template>
  <div id="app">
    <tab-bar></tab-bar>
  </div>
</template>

<script>
import TabBar from "components/common/TabBar";

export default {
  name: 'App',
  components: {
    TabBar
  }
}
</script>

<style>
  @import "assets/css/base.css";
</style>
