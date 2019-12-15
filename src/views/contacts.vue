<template>
  
  <div class="about">
    <Header></Header>
    <v-layout class="m-10 pa-50">
        <v-container class="pa-20 cont">
          <p class="display-3">Contacts</p>
          <div class="input-areas">
            <p class="display-1">We would like to hear from you</p>
            <v-form ref="form" v-model="valid" lazy-validation>
              <v-text-field color="#EF9A9A" class="inputs" v-model="name" :rules="nameRules" label="Name" required></v-text-field>
              <v-text-field color="#EF9A9A" v-model="email" :rules="emailRules" label="E-mail" required></v-text-field>
              <v-textarea color="#EF9A9A" v-model="message" :rules="messageRules" outlined label="Comment" class="textarea"></v-textarea>
              <v-btn depressed class="mr-6" @click="submit">submit</v-btn>
            </v-form>
          </div>
        </v-container>
    </v-layout>
    
  </div>
</template>

<script>
import Header from '../components/header.vue'
export default {
  components: {
    Header
  },

  valid: true,

  name: '',
  nameRules: [
    v => !!v || 'Name is required',
    v => (v && v.length <= 10) || 'Name must be less than 10 characters',
  ],

  email: '',
  emailRules: [
    v => !!v || 'E-mail is required',
    v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
  ],

  message: '',
  messageRules: [
    v => !!v || 'message is needed',
    v => (v && v.length <= 70) || 'Message must be less than 70 characters',
  ],
}

</script>

<style scoped>
.m-10 {
  
    display: flex;
    margin-left: -10rem !important;
}

.mr-6 {
    width: 100px;
    float: right;
}
.textarea {
  margin-top: 7px;
}

.cont {
  width: 40%;
  padding-top: 3.2rem;
}  

.display-3 {
    width: 80%;
    font-family: 'Satisfy', cursive !important;
    border-bottom: 3px solid #EF9A9A;
    padding-bottom: 1.3rem;
}

.input-areas {
  margin-top: 40px;
  background: #FFEEF2;
  padding: 50px;
  border-radius: 6px;
}

</style>