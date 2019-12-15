<template>
    <v-toolbar flat>
        <v-toolbar-title class="logo_cont">
          <v-img src="/favicon.ico" class="logo"></v-img>
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items class="mr-10 tool_items">
        <v-btn text class="toolbar-item" to="/">Home</v-btn>
        <v-btn text class="toolbar-item" to="/About">About</v-btn>
        <v-btn text class="toolbar-item" to="/recipe">Recipes</v-btn>
        <v-btn text class="toolbar-item" to="/contacts">Contacts</v-btn>
        </v-toolbar-items>

        <v-btn fab depressed small color="brown lighten-2" class="mr-2 white--text">F</v-btn>
        <v-btn fab depressed small color="brown lighten-2" class="mr-2 white--text">G</v-btn>
        <v-btn fab depressed small color="brown lighten-2" class="mr-4 white--text">T</v-btn>
    </v-toolbar>
</template>

<style scoped>
.logo_cont {
  position: relative;
  left: 2%;
  top: 1rem;
}

.logo {
  width: 100px !important;
}

.tool_items {
    background: #FFCDD2;
    border-radius: 7px;
}

.toolbar-item {
  text-transform: capitalize !important;
}

.toolbar-item:active,
.toolbar-item:hover
 {
   padding-bottom: 6px !important;
   text-decoration: underline !important;
   text-decoration-color: #EF9A9A !important;
}


</style>