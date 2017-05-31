<template lang="html">
  <div class="my-container">
    <header class="myHeader">
      <span v-on:click="back" class="back">返回</span>
      应用设置
    </header>
    <div class="mybox">
      <div class="mylist">
        <ul class="my-top">
          <li>
            <div class="list-box">
              <span>通知设置</span>
            </div>
          </li>
          <li>
            <div class="list-box listshead">
              <span>清楚缓存</span>
            </div>
          </li>
          <li>
            <div class="list-box">
              <span>去评价</span>
            </div>
          </li>
          <li>
            <div class="list-box">
              <span>关于</span>
            </div>
          </li>
        </ul>


        <ul class="my-bottom">
          <li>
            <div class="list-box list-box-align">
              <span>退出登录</span>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>

</template>

<script>
import { changeIndex } from "../vuex/action"
export default {
  data () {
    return {
    }
  },
  vuex: {
    actions: {
     change: changeIndex
   }
  },
  ready:function(){
    this.change(3);
  },
  methods:{
    back() {
      window.history.go(-1);
    }
  }
}
</script>
