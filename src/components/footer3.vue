<template>
    <div class="footer">
        <v-btn text color="#C0C0C0" to="/">
            <v-icon>mdi-arrow-left</v-icon>
            previous
        </v-btn>
        <v-btn text color="#C0C0C0" to="/home2">
            next
            <v-icon>mdi-arrow-right</v-icon>
        </v-btn>
    </div>
</template>

<style scoped>
    .footer {
        display: flex;
        padding-left: 10px !important;
        margin-top: 2% !important;
    }
</style>

