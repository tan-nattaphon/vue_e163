<template>
    <v-container>
        <h2>HELLO</h2>
        <h3>{{name}}  {{lastname}}</h3>
        <p>Age : {{age}}</p>
        <v-card style="padding: 0 10px; border-radius: 10px;">
            <br>
            <v-text-field
                v-model="name"
                label="First Name"
                placeholder="กรุณากรอกชื่อ ของท่าน"
                outlined
                shaped
            ></v-text-field>
            <v-text-field
                v-model="lastname"
                label="Last Name"
                placeholder="กรุณากรอกนามสกุล ของท่าน"
                outlined
                shaped
            ></v-text-field>
            <v-text-field
                v-model="age"
                label="Age"
                placeholder="กรุณากรอกอายุ ของท่าน"
                outlined
                shaped
            ></v-text-field>
        </v-card>
    </v-container>
</template>

<script>
export default {
    data:function(){
        return{
        name:"",
        lastname:"",
        age:"",

        }
    }
}
</script>