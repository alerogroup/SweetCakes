<template>
    <div class="recipe">
        <Header></Header>
        <p class="pt-12 display-3">Recipes</p>
        <v-container>
            <v-layout row wrap>
                <v-flex v-for="cake in cakes" :key="cake.name" dense class="flex-cont ma-2 pa-3"> 
                    <v-card flat :height="height" :width="width" class="card ma-5 pa-2" @click="toCake(cake.id)">
                        <v-img :height="height" :width="width" :src="cake.picture" class="images"></v-img>
                        <div class="red--text">{{ cake.name }}</div>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-container>
    </div>
</template>

<script>
    import Header from '../components/header.vue'
    export default {
        components: {
            Header
        }, 

        data() {
            return{
                height: 150,
                width: 200,

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
        },

        methods: {
            toCake(Id) {
                this.$router.push({name:'cake', params:{Pid:Id}})
            }
        }

    }
</script>

<style scoped>
.display-3 {
    font-family: 'Satisfy', cursive !important;
    border-bottom: 3px solid #EF9A9A;
    padding-bottom: 20px;
    width: 40%;
}

.seemore {
    text-transform: capitalize !important;
}

.flex-cont {
    flex: none;
}

.card {
    background: transparent;
}

.images {
    border: 1px solid #EF9A9A;
    border-radius: 3px;
}
</style>