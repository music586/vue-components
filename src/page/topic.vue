<template>
  <div class="content has-header">
    <div class="list">
    <a class="item item-avatar" href="#" v-for = "item in topics">
      <img :src = "item.author.avatar_url">
      <h2>{{ item.author.loginname}}</h2>
      <p>{{ item.title }}</p>
    </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'list',
  data () {
    return {
      topics: []
    }
  },
  created () {
    this.$http.get('https://cnodejs.org/api/v1/topics?tab=good').then(function (response) {
      this.topics = response.body.data
      console.log(response.body.data)
    }, function (response) {
      // debugger
    })
  }
}
</script>
