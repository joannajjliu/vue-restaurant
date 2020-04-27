<template>
    <v-container grid-list-lg>
        <v-layout row>
            <v-flex xs12 class="text-xs-center display-1 font-weight-black my-5">
                Available Meal Plans
            </v-flex>
        </v-layout>
        <v-layout row wrap v-for="item in menuItems" :key="item.name">
            <v-flex xs12 sm12 md4>
                <v-card>
                    <v-img :src="item.link" height="500px">
                        <v-container fill-height fluid>
                            <v-layout fill-height>
                                <v-flex xs12 align-end flexbox>
                                    <span class="headline white--text">KETO</span>
                                </v-flex>
                            </v-layout>
                        </v-container>
                    </v-img>

                    <v-card-title primary-title>
                        <div>
                            <h3 class="headline mb-0">{{item.title}}</h3>
                            <div>
                                {{item.description}}
                            </div>
                        </div>
                    </v-card-title>
                </v-card>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
export default {
    name: 'HomePlans',
    data: function () {
        return {
            menuItems: [
                {
                    title: "Keto",
                    description: "keto is tasty!",
                    link: "http://source.unsplash.com/hjCA3ecCXAQ"
                },
                {
                    title: "Paleo",
                    description: "paleo is tasty!",
                    link: "http://source.unsplash.com/6S27S6pZ6o0"
                },
                {
                    title: "Vegan",
                    description: "vegan is tasty!",
                    link: "http://source.unsplash.com/1SPu0KT-Ejg"
                },
            ]
        }
    }
};
</script>

<style scoped>
</style>