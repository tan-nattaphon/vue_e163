<template>
    <div>
        <h2>HELLO</h2>
        <p>{{name}}  {{lastname}}</p>
        <p>Age : {{age}}</p>
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
    </div>
</template>

