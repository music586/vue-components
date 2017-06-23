<template>
  <div>
    <h1>这是一个查询列表的例子</h1>
    <p>{{ demo }}</p>
  </div>
</template>

<script>
export default {
  name: 'list',
  data () {
    return {
      demo: 'this is demo'
    }
  },
  created () {
    this.$http.get('https://cnodejs.org/api/v1/topics', []).then(function (response) {
      debugger
    }, function (response) {
      debugger
    })
  }
}
</script>
