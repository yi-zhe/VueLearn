<template>
  <div class=".demo">
    <h2>学校名称: {{ name }}</h2>
    <h2>学校地址: {{ address }}</h2>
    <button @click="showName">点我提示学校名</button>
  </div>
</template>

<script>
// 默认暴露(一般都使用默认暴露)
export default {
  name: "School",
  data() {
    return {
      name: "学校名字",
      address: "通州",
    };
  },
  methods: {
    showName() {
      alert(this.name);
    },
  },
};

// 统一暴露
// export {school}
</script>

<style>
.demo {
  background-color: orange;
}
</style>