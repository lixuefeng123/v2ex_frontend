<template>
  <div class='uk-panel uk-panel-box'>
    <dl class='uk-description-list-line'>
      <dt>V2EX = way to explore</dt>
      <dd>V2EX 是一个关于分享和探索的地方</dd>
    </dl>
    <div class='uk-text-center inner line-top' v-if='! logined'>
      <a class='uk-button' v-link="{name: 'register'}">现在注册</a>
      <p>已注册用户请 <a v-link="{name: 'login'}">登录</a></p>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['logined'],
    methods: {
      category: function (tab) {
        this.$dispatch('tab', tab)
      }
    }
  }
</script>
