<template>
  <div>
    <h3>Hello: {{ name }}</h3>
    <h3>age: {{ age }}</h3>
    <input type="text" :value="name">
    <input type="text" v-model="name">
    <button @click="doSave">SAVE</button>
    <button @click="doMenu">MAIN MENU</button>
    <button @click="doHome">HOME</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "Nattaphon Khopuangklang",
      age: 20,
    }
  },
methods:{
    doSave(){
        console.log("DO Save");
        },
    doMenu(){
        this.$router.push('menu');
        },
    doHome(){
        this.$router.replace('/');
        },
    },
}
</script>