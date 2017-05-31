<template lang="html">
<div class="my-container">
  <header class="myHeader">
    <span @click='back' class="back">返回</span>
    我的地址簿
  </header>
  <div class="order">
    <image src="./images/address.png" />
    <span class="text">您还没有收货地址</span>
    <div class="button">去添加</div>
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
