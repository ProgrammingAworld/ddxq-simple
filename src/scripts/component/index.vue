<template>
    <div id="main-box">
      <div class="index-container">
        <router-view></router-view>
      </div>
      <div id="footer">
        <ul>
          <li
            v-bind:class="cur == $index ? 'active' : ''"
            v-for="tab in tablist"
            v-link="{path:tab.path}">
            <i class="iconfont">{{{tab.icon}}}</i>
            <b>{{tab.name}}</b>
          </li>
        </ul>
      </div>
    </div>
</template>

<script>
import  {getIndex}  from '../vuex/getters'
export default {
    data() {
        return {
            tablist:[
              {path: '/index/service', icon: '&#xe684;', name: '生活服务'},
              {path: '/index/neighbor', icon: '&#xe68f;', name: '邻居'},
              {path: '/buycar', icon: '&#xe664;', name: '购物车'},
              {path: '/index/my', icon: '&#xe623;', name: '我'}
            ]
        }
    },
    vuex: {
      getters: {
        // 注意在这里你需要 `getCount` 函数本身而不是它的执行结果 'getCount()'
        cur: getIndex
      }
    },
    ready:function(){

    },
    methods:{

    }
}
// {path: '/index/service', icon: '&#xe684;', name: '生活服务'},
// {path: '/index/neighbor', icon: '&#xe68f;', name: '邻居'},
// {path: '/index/my', icon: '&#xe623;', name: '我'}
</script>
