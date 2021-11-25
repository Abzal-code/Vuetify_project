<template>
    <v-row>
        <v-col class="cafe__component">
            <h1 class="py-4">Lists of cafes</h1>

            <v-row class="cafe__list mx-2">
                <v-col v-for="cafe in cafes" :key="cafe.id" md="4">
                    <v-card class="cafe__card">

                        <v-img
                            height="250"
                            :src="cafe.img"
                        ></v-img>

                        <v-card-title>
                            <router-link to="/cafe/view">
                                {{ cafe.name }}
                            </router-link>
                        </v-card-title>

                        <v-card-text>
                            <p>{{ cafe.description }}</p>
                            <h4>Rating: {{ cafe.rating }} of 5</h4>
                        </v-card-text>
                    </v-card>
                </v-col>
            </v-row>
        </v-col>
    </v-row>
</template>

<script>
    export default {
       name: 'Cafe',
       data: () => ({
           cafes: [
               {
                   id: 0,
                   name: 'K-FOOD',
                   description: 'Here we cooking nice korean food',
                   img: 'https://thekitchencommunity.org/wp-content/uploads/2021/02/43-Foods-That-Start-With-E-1200x675.jpg',
                   tags: ['korean'],
                   rating: 5
               },
               {
                   id: 1,
                   name: 'Italian pasta',
                   description: 'Here you can find Italian pasta',
                   img: 'https://i0.hippopx.com/photos/120/420/848/food-lip-delicious-food-preview.jpg',
                   tags: ['Italian'],
                   rating: 5
               },
               {
                   id: 2,
                   name: 'Kazakh Meat',
                   description: 'Youll falling love when your tasty our horse meat',
                   img: 'https://www.aveneerdmc.com/sites/default/files/be_inspired_cuisine_2.jpg',
                   tags: ['kazakh'],
                   rating: 5
               },
               {
                   id: 3,
                   name: 'Chinese',
                   description: 'If love Chinese food, you know we are the best',
                   img: 'https://www.alaturka.info/images/leben/kulinarisches/zwiebelkuchen.jpg',
                   tags: ['chinese'],
                   rating: 4
               },
               {
                   id: 4,
                   name: 'Love from Paris',
                   description: 'The best delicious from French',
                   img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQjW1DO_3oi9qJZvAePhWFRL2UEHDgo2JZkCw&usqp=CAU',
                   tags: ['french'],
                   rating: 5
               },
               {
                   id: 5,
                   name: 'Switzerland cheese',
                   description: 'You must to know Whats cheese of Switzerland',
                   img: 'https://img.traveltriangle.com/blog/wp-content/uploads/2018/11/cover-for-Chicago-Food.jpg',
                   tags: ['switzerland'],
                   rating: 5
               },
           ]
       }), 
    }
</script>
