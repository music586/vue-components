<template>
  <div class="content has-header">
    <div class="list card">
    <a class="item item-icon-left" href="#" v-for = "item in topicList" :key = "item.tabCode">
     <i class="icon"  :class="item.tabIconClass" ></i>
     {{ item.tabName }}
    </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'list',
  data () {
    return {
      topicList: [{
        tabName: '全部',
        tabCode: '',
        tabIconClass: 'ion-stats-bars'
      }, {
        tabName: '精华',
        tabCode: 'good',
        tabIconClass: 'ion-fireball'
      }, {
        tabName: '分享',
        tabCode: 'share',
        tabIconClass: 'ion-share'
      }, {
        tabName: '问答',
        tabCode: 'ask',
        tabIconClass: 'ion-chatbubble-working'
      }, {
        tabName: '招聘',
        tabCode: 'job',
        tabIconClass: 'ion-coffee'
      }, {
        tabName: '客户端测试',
        tabCode: 'dev',
        tabIconClass: 'ion-wand'
      }]
    }
  },
  created () {
  }
}
</script>
<style>
.content .card {
    padding-top: 1px;
    padding-bottom: 1px;
    box-shadow: 0 1px 1px rgba(0, 0, 0, 0.1); 
  }
.list .icon {
  border-width:0px;
  font-size: 28px;
}
.item{
  padding:15px 40px 15px 54px ;
}
.list:last-child.card {
    margin-bottom: 48px;
}
</style>
