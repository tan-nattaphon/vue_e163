<template>
  <v-data-table :headers="headers" :items="card" :items-per-page="5" class="elevation-1"></v-data-table>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        {
          text: "ID",
          align: "start",
          sortable: false,
          value: "id",
        },
        { text: "CODE-CARD", value: "card_code" },
        { text: "สถานะบุคคล", value: "ref_type" },
        { text: "CODE", value: "ref_code" },
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
      console.log("list Card");
      let res = await fetch("http://localhost:7001/listCard");
      let data = await res.json();
      console.log("data", data.rows);
      this.card = data.rows[0];
    },
  },
};
</script>