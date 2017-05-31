<template lang="html">
<div class="my-container">
  <header class="myHeader">
    <span @click='back' class="back">返回</span>
    我的订单
  </header>
  <div class="order">
    <image src="./images/order.png" />
    <span class="text">暂无相关订单</span>
    <div class="button">去逛逛</div>
  </div>
</div>
</template>

<script>
export default {
  data () {
    return {}
  },
  computed: {},
  mounted () {},
  methods: {
    back(){
      window.history.go(-1);
    }
  },
  components: {}
}
</script>

<style lang="css">
</style>
