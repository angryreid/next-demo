
<template>
  <div>
    <div>{{info.name}}</div>
    <div>{{info.age}}</div>
  </div>
</template>
<script>
import axios from "axios";
export default {
  data() {
    return {
      name: "hello"
    };
  },
  asyncData() {
    return axios.get("https://api.myjson.com/bins/x4zy7").then(res => {
      return { info: res.data };
    });
  }
};
</script>