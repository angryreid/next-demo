<template>
  <div>
    <h2>News index page</h2>
    <p>NewsId: {{$route.params.newsId}}</p>
    <ul>
      <li>
        <nuxt-link :to="{name: 'index'}">HOME</nuxt-link>
      </li>
      <li>
        <nuxt-link :to="{name: 'about'}">ABOUT</nuxt-link>
      </li>
    </ul>
    <ul>
      <!-- <li>
        <a href="/news/123">news-123</a>
      </li>
       <li>
        <a href="/news/456">news-456</a>
      </li> -->
      <!-- 动态路由传参数 -->
      <li>
        <nuxt-link :to="{name: 'news-id', params: {id: 123,title: 'You are very good!'}}">news-123</nuxt-link>
      </li>
      <li>
        <nuxt-link :to="{name: 'news-id', params: {id: 456}}">news-456</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  transition: "single"
}
</script>