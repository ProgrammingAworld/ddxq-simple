<template lang="html">
 <div class="commission-container">
   <header class="header">
     <div class="iconfont3" @click="back">&#xe611;</div>
     <h1>代办事</h1>
   </header>
   <div id="cleariscroll">
     <div class="top-bg">
       <img src="/android_asset/www/images/commisstion1.png" alt="" />
     </div>
     <div class="clear-tit">
       <img src="/android_asset/www/images/daishop.png" alt="" />
     </div>
     <ul class="clearele">
       <li v-for='item in clearlist' v-show="item.src!=''">
         <img v-bind:src="item.src" alt="" />
         <div class="toptext">
           <i>{{item.tit}}<img v-bind:src="item.hotimg" alt="" /></i>
           <em>{{item.discribe}}</em>
         </div>
       </li>
     </ul>
     
     <div class="clear-tit">
       <img src="/android_asset/www/images/daishop.png" alt="" />
     </div>
     <ul class="clearhome">
       <li v-for='item in clearlist2' v-show="item.src!=''">
         <img v-bind:src="item.src" alt="" />
         <div class="toptext">
           <i>{{item.tit}}</i>
           <em>{{item.discribe}}</em>
         </div>
       </li>
     </ul>
   </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      clearlist:[],
      clearlist2:[]
    }
  },
  ready:function(){
    this.$http.get('./mock/commission1.json')
    .then((res)=>{
    var resData = "";
    try {
      resData = JSON.parse(res.data);
    }catch (e) {
      resData = res.data;
    }
      this.clearlist=resData;
    })
    this.$http.get('./mock/clear2.json')
    .then((res)=>{
    var resData = "";
    try {
      resData = JSON.parse(res.data);
    }catch (e) {
      resData = res.data;
    }
      this.clearlist2=resData;
    })
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
