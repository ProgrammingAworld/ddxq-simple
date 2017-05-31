<template lang="html">
<div class="coupon my-container">
  <header class="myHeader">
    <span @click='back' class="back">返回</span>
    我的优惠券
  </header>
  <div class="coupon-container">
    <ul>
      <li v-for="coupon in couponList ">
        <image src="./images/coupon.png" alt="优惠券" class="img-coupon">
        <div>
          <span>￥<span class="money">{{coupon.money}}</span></span>
          <span class="use">{{coupon.use}}</span>
        </div>
        <image src="./images/timeout.png" alt="图片未能正确显示" class="img-timeout">
      </li>
    </ul>
  </div>
</div>
</template>

<script>
export default {
  data () {
    return {
      couponList:[{
        money:6,
        use:'满30元使用'
      },{
        money:8,
        use:'满35元使用'
      },{
        money:2,
        use:'满20元使用'
      },{
        money:198,
        use:'满200元使用'
      },{
        money:10,
        use:'满100元使用'
      }]
    }
  },
  methods: {
    back(){
      window.history.go(-1);
    }
  }
}
</script>
