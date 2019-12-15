<template>
  <div class="home">
    <Header></Header>
    <v-layout class="m-10 pa-50">
        <v-container class="cupcake">
          <div color="#C0C0C0" class="font-italic">Cheesecake</div>
        </v-container>

        <v-container class="imagecake">
          <v-img :src="potrait" class="pa-20"></v-img>
        </v-container>

        <v-container class="cont">
          <p class="cont-title">{{ name }}</p>
          <v-layout row wrap>
            <v-flex>
              <v-card  flat class="ma-3">
                <v-card-text>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim ea distinctio pariatur quas fuga qui nisi eius, earum repellat consequuntur!</v-card-text>
                <v-card-text>{{ contacts }}</v-card-text>

                <v-card-actions>
                  <v-btn depressed rounded color="#E57373" class="readmore">Read More...</v-btn>
                </v-card-actions>
              </v-card>
            </v-flex>
          </v-layout>

          <v-card flat color="#FFCDD2" class="edge">
            <v-card-title class="titleLorem">Lorem Ipsum</v-card-title>
            <v-card-text>{{ bio }}</v-card-text>
          </v-card>
        </v-container>
    </v-layout>
    <Footer></Footer>
  </div>
</template>


<script>
import Header from '../components/header1.vue'
import Footer from '../components/footer.vue'
export default {
    components: {
      Header,
      Footer
    },

    data: () => ({
        potrait: '/cheesecake.png',
        bio: 'Lorem ipsum dolor sit amet,  quaerat magnam delectus amet earum facere nobis ad voluptas veniam, ipsum omnis. Labore, labore ut reiciendis.',
    })
  }

</script>

<style scoped>
.cupcake {
  font-family: 'Playfair Display', serif;
  transform: rotate(90deg);
  height: 32rem !important;
  margin-top: 14rem;
  margin-left: -30%;
  font-size: 4.7rem;
  color: #C0C0C0;
}

.readmore {
  width: 10rem;
  text-transform: capitalize !important;
}

.pa-20 {
    height: 25rem !important;
    width: 31rem;
    margin-top: 5rem;
    margin-left: -7%;
    border-radius: 8px;
}

.cont {
  width: 30%;
  padding-top: 3rem;
  margin-right: 5rem;

}

.cont-title {
    font-family: 'Satisfy', cursive !important;
    border-bottom: 3px solid #EF9A9A;
    padding-bottom: 1.3rem;
    padding-top: 1.3rem;
    width: 60%;
}

.edge {
  position: relative;
  justify-content: center;
  border-radius: 6px !important;
  width: 300rem;
  margin-top: 20%;
  margin-left: 30%;
  padding: 3.2rem;
}

.contact {
    color: #FFCDD2 !important;
}

.titleLorem {
  font-family: 'Satisfy', cursive !important;
}

</style>