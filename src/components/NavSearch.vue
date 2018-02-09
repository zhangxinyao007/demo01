<template lang="pug">
  div#search.search-warp
    div.pa.searchTags
      a(v-for="tag in searchTags", :href="tag.url", target="_blank") {{tag.name}}
    div.search-area
      input.search-input(type="text" autocomplete="off")
      input.btn_search(type="hidden")

    div.showhide-search
</template>

<script>
export default {
  data () {
    return {
      searchTags: [
        {name: '前端入门', url: '//class.imooc.com/sc/20'},
        {name: 'Java小白入门', url: '//class.imooc.com/sc/18'}
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .search-warp
    float left
    margin-left 24px
    height 48px !important
    margin-top 12px
    min-width 32px
    position absolute
    .pa
      position absolute
    .searchTags
      z-index 100
      top 12px
      bottom 24px
      left unset
      right 40px
</style>
