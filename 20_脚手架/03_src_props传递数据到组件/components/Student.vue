<template>
  <div>
    <h1>{{ msg }}</h1>
    <h2>学生姓名: {{ name }}</h2>
    <h2>学生年龄: {{ sex }}</h2>
    <h2>学生年龄: {{ myAge + 1 }}</h2>
    <button @click="updateAge">更新年龄</button>
  </div>
</template>

<script>
// 默认暴露(一般都使用默认暴露)
export default {
  name: "Student",
  data() {
    return {
      msg: "我是一个学生",
      myAge: this.age
    }
  },
  methods: {
    updateAge() {
      this.myAge++
    }
  },
  // 简单声明接收
  // props: ["name", "sex", "age"]
  // 接收的同时对数据进行类型限制
  // props: {
  //   name: String,
  //   age: Number,
  //   sex: String,
  // }
  // 接收数据同时对数据: 类型限制 默认值处理 是否必传限制
  props: {
    name: {
      type: String,
      required: true,
    },
    sex: {
      type: String,
      required: true,
    },
    age: {
      type: Number,
      required: false,
      default: 99,
    },
  },
};

// 统一暴露
// export {school}
</script>
