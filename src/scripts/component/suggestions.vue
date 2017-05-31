<template lang="html">
<div class="my-container">
  <header class="myHeader">
    <span @click='back' class="back">返回</span>
    意见与建议
    <span class="submit">提交</span>
  </header>
  <textarea class="textarea" placeholder="我们想听听你的新生，如果愿意，你也可以留下联系方式，我们期待与你真诚沟通。"></textarea>
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
