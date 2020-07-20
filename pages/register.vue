<template>
    <v-card>
        <center>
            <h2>REGISTER</h2>
        </center>
        <v-card-text>
            <v-form>
                <v-text-field  prepend-icon="mdi-account-circle" label="Username" />
                <v-text-field  prepend-icon="mdi-account-circle" label="Password" />
                <v-text-field  prepend-icon="mdi-account-circle" label="Address" />
                <v-text-field  prepend-icon="mdi-account-circle" label="Tel"/>
                <v-btn color="primary">ENTER</v-btn>
                <v-btn color="red">CANCEL</v-btn>
            </v-form>
        </v-card-text>
    </v-card>
</template>