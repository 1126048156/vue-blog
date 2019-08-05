<template>
    <header id="header">
      <div class="navbox">
        <h1 class="logo">
          <a href="#">徐青青的个人博客</a>
        </h1>
        <nav>
          <ul id="starlist">
            <li><a href="#">首页</a></li>
            <li><a href="#">个人博客日记</a></li>
            <li><a href="#">博客网站制作</a></li>
            <li>
              <a href="#">网页设计心得</a>
              <ul class="sub">
                <li><a href="#">推荐工具</a></li>
                <li><a href="#">css</a></li>
                <li><a href="#">html</a></li>
                <li><a href="#">js</a></li>
                <li><a href="#">vue</a></li>
              </ul>
            </li>
            <li><a href="#">优秀个人博客</a></li>
            <li><a href="#">关于我</a></li>
          </ul>
        </nav>
        <div class="searchico"></div>
      </div>
    </header>
</template>

<script>
    export default {
        name: "Header",
        data() {
            return {}
        }
    }
</script>

<style scoped>

</style>
