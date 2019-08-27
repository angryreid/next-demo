<template>
  <section class="container">
    <div>
      <img class="cat" src="~/assets/img/cat.jpg" alt="">
      <ul>
        <li>
          <nuxt-link :to="{name: 'index'}">HOME</nuxt-link>
        </li>
        <li>
          <nuxt-link :to="{name: 'about'}">ABOUT</nuxt-link>
        </li>
        <li>
          <!-- 传递参数 -->
          <nuxt-link :to="{name: 'news', params: {newsId: 1}}">NEWS</nuxt-link>
        </li>
        <li>
          <nuxt-link :to="{name: 'data'}">DATA</nuxt-link>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import AppLogo from "~/components/AppLogo.vue";

export default {
  components: {}
};
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

