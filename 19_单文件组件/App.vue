<template>
  <div>
    <School></School>
    <student></student>
  </div>
</template>

<script>
import School from "./School";
import Student from "./Student";
import Student from "./Student.vue";

export default {
  name: "App",
  components: {
    School,
    Student,
  },
};
</script>
