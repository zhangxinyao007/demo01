<template lang="pug">
  header#NavHeader
    div.page-container
      div.logo
        a(href="/" target="_self" title="首页")
          img(src="../assets/logo.png" title="慕课网")
      ul.nav-item.clearfix
        li(v-for="item in navList")
          a(:href="item.url" target="_self") {{item.name}}
            i.icn-new(v-if="item.name == '职业路径'")
      nav-search
</template>

<script>
import NavSearch from './NavSearch'

export default {
  data () {
    return {
      navList: [
        {name: '免费课程', url: '/course/list'},
        {name: '职业路径', url: '/course/list'},
        {name: '实战', url: '/course/list'},
        {name: '猿问', url: '/course/list'},
        {name: '发现', url: '/course/list'}
      ]
    }
  },
  components: {
    NavSearch
  }
}
</script>

<style lang="stylus" scoped>
  #NavHeader
    height 72px
    background #FFF

  .page-container
    padding-right 10px
    z-index 900
    box-shadow 0 4px 8px 0 rgba(7,17,27,.1)
    height 72px

  .logo
    margin 0 28px 0 24px
    float left
    a
      img
        height 72px
  .nav-item
    li
      float left
    a
      padding 0 20px
      display block
      color #4D555D
      text-align center
      font-size 16px
      line-height 72px
      -webkit-transition background-color .3s
      -moz-transition background-color .3s
      transition background-color .3s
      height 72px
      postion relative
    .icn-new
      position relative
      display inline-block
      top -10px
      width 16px
      height 16px
      background url(../assets/new.png) no-repeat

</style>
