<template>
    <div>
        <v-row>
            <v-col>
                <v-breadcrumbs :items="breadcrumbs_items"></v-breadcrumbs>
            </v-col>
        </v-row>
        <v-row>
            <v-col md="5">
                <v-card>

                    <v-img 
                        height="350"
                        src="https://miro.medium.com/focal/1200/1200/82/47/1*njE2UVPnj-p4G-x6kYWIhw.jpeg"
                        class="d-flex align-end"
                    >
                        <v-card-title>
                            <h2 class="text-h2 white--text">K-Food</h2>
                        </v-card-title>

                    </v-img>

                </v-card>
            </v-col>
            <v-col md="7">
                <v-card class="h-100">
                    <v-card-text>
                        <h4 class="text-h5 mb-4">
                            Come here if you wanna to taste cool ramen
                        </h4>
                        <v-divider/>
                        <p class="mt-4 text-body-1 mr-5">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis quaerat aut nisi tempora, totam fuga eius expedita quisquam, fugiat, nam quidem? Ipsam expedita sed quod, ducimus earum ab at voluptas. Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis quaerat aut nisi tempora, totam fuga eius expedita quisquam, fugiat, nam quidem? Ipsam expedita sed quod, ducimus earum ab at voluptas.
                        </p>
                    </v-card-text>
                </v-card>
            </v-col>
        </v-row>

        <v-row class="cafe__menu">
            <v-col md="6">
                <v-card>
                    <v-img  height="450"
                            src="https://eatforum.org/content/uploads/2018/05/table_with_food_top_view_900x700.jpg"
                            class="flex align-end"
                    >
                        <v-card-title>
                            <h2 class="text-h2 white--text">Menu</h2>
                        </v-card-title>
                    </v-img>
                </v-card>
            </v-col>
            <v-col md="6">
                <v-card>
                    <v-card-text>
                        <v-list-item-group>
                            <v-list-item v-for="item in menu_items" :key="item.id">
                                <v-list-item-avatar>
                                    <v-img :src="item.img"></v-img>
                                </v-list-item-avatar>
                                <v-list-item-content>
                                        <v-list-item-title class="text-subtitle-1">
                                            {{ item.title }}
                                        </v-list-item-title>
                                        <v-list-item-subtitle class="text-body-1">
                                            {{ item.price }}
                                        </v-list-item-subtitle>
                                    </v-list-item-content>

                                    <v-list-item-action>
                                        <v-btn icon>
                                            <v-icon color="grey lighten-1">mdi-plus</v-icon>
                                        </v-btn>
                                    </v-list-item-action>
                            </v-list-item>
                        </v-list-item-group>
                    </v-card-text>
                    
                </v-card>
            </v-col>
        </v-row>

        <cafe-comment></cafe-comment>
    </div>
</template>

<script>
import CafeComment from './CafeComment.vue'
export default {
    components: { CafeComment },
    name: 'Cafe-view',
    data: () => ({
        breadcrumbs_items: [
            {
                text: 'Home',
                disabled: false,
                href: '/'
            },
            {
                text: 'K-FOOD',
                disabled: true,
                href: '/cafe/view' 
            }
        ],
        menu_items: [
            {
                id: 0,
                title: 'Sapporo Miso Ramen',
                img: 'https://cdn.pixabay.com/photo/2020/02/28/12/43/bibimbap-4887417_1280.jpg',
                price: 35.69
            },
            {
                id: 1,
                title: 'Hakata Tonkotsu Ramen',
                img: 'https://upload.wikimedia.org/wikipedia/commons/thumb/f/f5/Korean.food-Bibimbap-02.jpg/1280px-Korean.food-Bibimbap-02.jpg',
                price: 25.69
            },
            {
                id: 2,
                title: 'Kitakata Ramen',
                img: 'https://inmykorea.com/wp-content/uploads/2021/08/Untitled-design-2021-08-16T135922.914.jpg',
                price: 31.69
            },
            {
                id: 3,
                title: 'Wakayama Ramen',
                img: 'http://saltoalto06.com/wp-content/uploads/2019/03/Budae-Jjigae-1024x678.jpg',
                price: 29.69
            },
        ],
    }),
}
</script>

<style scoped type="text/css">
    .h1-100 {
        height: 100%;
    }
</style>