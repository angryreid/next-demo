<template>
  <div>
    <h2>News detail</h2>
    <p>NewsID: {{$route.params.id}}</p>
    <ul>
      <li>
        <nuxt-link :to="{name: 'index'}">HOME</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  // 路由参数校验
  validate({ params }) {
    console.log(params.id);
    console.log(/^\d+$/.test(params.id));
    return /^\d+$/.test(params.id);
  },
  data() {
    return {
      title: this.$route.params.title
    };
  },
  // 设置单个页面独立头部信息
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: "description",// 唯一标示
          name: "news-123",
          content: "this is a news page!"
        }
      ]
    };
  }
};
</script>