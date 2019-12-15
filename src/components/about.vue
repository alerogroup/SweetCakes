<template>
  <div class="details">
    <Header />
    
    <div v-for="(person, index) in team" :key="index">
        <div v-if="proId == person.id" class="d-flex justify-space-around">
            <img :src="person.avatar" class="image">
            <div class="image-cont">
                <p class="display-3">{{person.name}}</p>
                <div>
                    <v-card flat class="ma-3">
                        <v-card-text>
                            {{ person.bio}}
                        </v-card-text>
                        <v-card-title>
                            Contacts
                        </v-card-title>
                        <v-card-text>
                            {{person.contacts}}
                        </v-card-text>
                    </v-card>
                </div>
            </div>
        </div>
    </div>
    <v-btn dark depressed class="btn" color="pink lighten-4" to="/About">Back</v-btn>

    
  </div>
</template>

<script>
import Header from '../components/header'

export default {

    name: 'about',
    components: {
        Header
    },
    
    data() {
        return {
            proId: this.$route.params.Pid,
            width: 200,
            height: 200,

            //team details
            team: [
                {id: 1, name: 'Jane Oloo', role: 'Co-Founder/CEO', avatar: '/potrait.jpg', bio: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Commodi laboriosam, excepturi, quisquam tempore cum quibusdam tenetur exercitationem odit nesciunt quis saepe explicabo quaerat fugiat eos eveniet, provident ea! Vero quo perspiciatis at quam similique quod excepturi tempore culpa nulla itaque dignissimos non cumque quaerat magnam delectus amet earum facere nobis ad voluptas veniam, ipsum omnis. Labore, debitis? Commodi, eum. Laborum expedita distinctio, nesciunt necessitatibus rem suscipit perferendis, tempora et cumque nobis corrupti sapiente qui deleniti asperiores commodi labore ut reiciendis.', contacts: 'Lorem ipsum dolor'},

                {id: 2, name: 'Janice Mwendwa', role: 'Head Pastry Chef', avatar: '/portrait1.jpg', bio: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Commodi laboriosam, excepturi, quisquam tempore cum quibusdam tenetur exercitationem odit nesciunt quis saepe explicabo quaerat fugiat eos eveniet, provident ea! Vero quo perspiciatis at quam similique quod excepturi tempore culpa nulla itaque dignissimos non cumque quaerat magnam delectus amet earum facere nobis ad voluptas veniam, ipsum omnis. Labore, debitis? Commodi, eum. Laborum expedita distinctio, nesciunt necessitatibus rem suscipit perferendis, tempora et cumque nobis corrupti sapiente qui deleniti asperiores commodi labore ut reiciendis.', contacts: 'Lorem ipsum dolor'}
            ]
        }
    }
}

</script>

<style scoped>
.image {
    height: 34rem !important;
} 

.image-cont {
  width: 50%;
}

.display-3 {
    font-family: 'Satisfy', cursive !important;
    border-bottom: 3px solid #EF9A9A;
    padding-bottom: 1.3rem;
    width: 60%;
}

.contact {
    color: #EF9A9A !important;
}

.btn {
    position: absolute;
    top: 90%;
    right: 5%;
}

.d-flex {
    position: absolute;
    top: 20%;
}
</style>