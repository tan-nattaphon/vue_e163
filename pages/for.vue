<template>
  <div>
    <h1>Student List</h1>
    <ul>
      <li v-for="st in student" :key="st.code">
        <span>{{ st.GPA }}</span>
        <span>{{ st.name }}</span>
        <span>{{ st.lastname }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      student: [],
    };
  },
  created() {
    this.listStudent();
  },
  methods: {
    async listStudent() {
      console.log("list std");
      let res = await fetch("http://localhost:7001/listStd");
      let data = await res.json();
      console.log("data", data.data[0]);
      this.student = data.data[0];
    },
  },
};
</script>