<template>
  <div>
    <div>
      <h1>Student List</h1>
      <ul>
        <li v-for="cr in card" :key="cr.card_code">
          <span>{{ cr.card_code }}</span>
          <span>{{ cr.ref_type }}</span>
          <span>{{ cr.ref_code }}</span>
          <span>{{ cr.is_active }}</span>
          <v-btn color="warning" @click="edit(cr.card_code)">EDIT</v-btn>
          <v-btn color="red" @click="del(cr.card_code)">DEL</v-btn>
        </li>
      </ul>
    </div>
    <nuxt-link to="form_list_std">
      <v-btn color="warning">Student List</v-btn>
    </nuxt-link>
    <nuxt-link to="add_card">
      <v-btn color="success">ADD</v-btn>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        {
          text: "รหัส",
          align: "start",
          sortable: false,
          value: "card_code",
        },
        { text: "ชนิดผู้ใช้", value: "ref_type" },
        { text: "code", value: "ref_code" },
        { text: "สถานะ", value: "is_active" },
      ],
      card: [],
    };
  },
  created() {
    this.listCard();
  },
  methods: {
    async listCard() {
      console.log("List Success");
      let res = await fetch("http://localhost:7001/listCard");
      let data = await res.json();
      console.log("data", data);
      this.card = data.rows;
    },
    edit(card_code) {
      console.log("card_code=", card_code);
      this.$router.push("edit_card?card_code=" + card_code);
    },
    async del(card_code) {
      console.log("card_code=", card_code);
      let res = await this.$http.post(
        "http://localhost:7001/delcard?card_code=" + card_code
      );
    },
  },
};
</script>