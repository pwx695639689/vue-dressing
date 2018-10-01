<template>
  <div>
    <div class="price" v-for="item of price" :key="item.id">
      <div class="price-num">￥{{item.num}}</div>
      <div class="price-out">已售{{item.out}}</div>
    </div>
    <div class="head" v-for="item of product" :key="item.id">
      <div class="head-desc">{{item.desc}}</div>
      <div class="head-title">{{item.title}}</div>
    </div>
    <div class="item" v-for="(item, index) of list" :key="index">
      <div class="item-title">
        <span class="item-title-icon">#</span>
        {{item.title}}
      </div>
      <div class="item-desc">{{item.desc}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    list: Array,
    price: Array,
    product: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .price
    display: flex
    line-height: .5rem
    margin-top: .2rem
    padding: 0 .2rem
    justify-content: space-between
    .price-num
      font-size: .4rem
      font-weight: bold
      color: $bgColor
    .price-out
      font-size: .25rem
      color: #666
  .head
    margin-top: .4rem
    .head-desc
      font-size: .28rem
      color: #666
      line-height: .28rem
      padding: .1rem .1rem
    .head-title
      font-size: .35rem
      line-height: .4rem
      padding: .2rem .1rem
      font-weight: bold
  .item
    margin-top: .5rem
    .item-title
      line-height: .8rem
      font-size: .35rem
      margin-left: .2rem
      color: $bgColor
      font-weight: bold
    .item-desc
      line-height: .3rem
      word-wrap: break-word
      padding: .2rem
</style>
