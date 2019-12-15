<template>
   <div class="view-details">
     <Header />
      <div v-for="(item,index) in cakes" :key="index">
        <div v-if="Id == item.id" class="d-flex justify-space-around align-center">
          <img :src="item.picture" class="image ma-4">
          <div class="pa-6">
            <h1>{{ item.name }}</h1>
            {{ item.recipe }}
          </div>          
        </div>    
      </div>

      <!-- back button-->
      <v-btn color="pink lighten-3" class="btn" text to="/recipe">
        <v-icon>mdi-arrow-left</v-icon>Back
      </v-btn>
   </div>
</template>

<script>
import Header from '@/components/header2.vue'

export default {
  components: {
    Header
  },

  name: 'cake',
    data() {
      return { 
        Id:this.$route.params.Pid,

        cakes: [
          {id: 1, picture: '/cake.jpeg', name: 'Lorem Ipsum', recipe: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque nesciunt qui, labore odit sed sint impedit vero?', isHidden: false},
          {id: 2, picture: '/cake1.jpeg', name: 'Lorem Ipsum', recipe: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque nesciunt qui, labore odit sed sint impedit vero?', isHidden: false},
          {id: 3, picture: '/cake2.jpeg', name: 'Lorem Ipsum', recipe: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque nesciunt qui, labore odit sed sint impedit vero?', isHidden: false},
          {id: 4, picture: '/cake3.jpeg', name: 'Lorem Ipsum', recipe: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque nesciunt qui, labore odit sed sint impedit vero?', isHidden: false},
          {id: 5, picture: '/cake4.jpeg', name: 'Lorem Ipsum', recipe: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque nesciunt qui, labore odit sed sint impedit vero?', isHidden: false},
          {id: 6, picture: '/cake5.jpeg', name: 'Lorem Ipsum', recipe: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque nesciunt qui, labore odit sed sint impedit vero?', isHidden: false},
          {id: 7, picture: '/cake6.jpeg', name: 'Lorem Ipsum', recipe: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque nesciunt qui, labore odit sed sint impedit vero?', isHidden: false},
          {id: 8, picture: '/cake7.jpeg', name: 'Lorem Ipsum', recipe: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque nesciunt qui, labore odit sed sint impedit vero?', isHidden: false},
          {id: 9, picture: '/cake1.jpg', name: 'Lorem Ipsum', recipe: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque nesciunt qui, labore odit sed sint impedit vero?', isHidden: false},
          {id: 10, picture: '/cupcake.jpeg', name: 'Lorem Ipsum', recipe: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque nesciunt qui, labore odit sed sint impedit vero?', isHidden: true}
        ]
      }
    }
}
</script>

<style scoped>
.image {
  height: 20rem;
  width: 30%;
}

.pa-6 {
  width: 40%;
}

.image {
  border-radius: 6px;
}

.d-flex {
  margin-top: 5%;
}

.btn {
  position: relative;
  left: 60%;
}
</style>

