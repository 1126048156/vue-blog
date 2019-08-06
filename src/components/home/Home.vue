<template>
    <div>
      <home-header></home-header>
      <home-search></home-search>
    </div>
</template>

<script>
  import HomeHeader from "@/common/Header"
  import HomeSearch from "@/common/Search"
    export default {
        name: "Home",
        data() {
            return {}
        },
      components:{
          HomeHeader,
          HomeSearch
      }
    }
</script>

<style scoped>

</style>
