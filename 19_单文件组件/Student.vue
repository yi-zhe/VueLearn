<template>
  <div>
    <h2>学生姓名: {{ name }}</h2>
    <h2>学生年龄: {{ age }}</h2>
  </div>
</template>

<script>
// 默认暴露(一般都使用默认暴露)
export default {
  name: "Student",
  data() {
    return {
      name: "张三",
      age: 18,
    };
  },
  methods: {
  },
};

// 统一暴露
// export {school}
</script>

<style>
</style>