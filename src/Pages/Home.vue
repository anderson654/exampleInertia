<template>
    <v-card>
        <v-layout>
            <v-navigation-drawer
                v-model="drawer"
                :rail="rail"
                permanent
                @click="rail = false"
            >
                <v-list-item
                    prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
                    title="John Leider"
                    nav
                    style="height: 64px"
                    class="elevation-3 rounded-0"
                >
                    <template v-slot:append>
                        <v-btn
                            variant="text"
                            icon="mdi-chevron-left"
                            @click.stop="rail = !rail"
                        ></v-btn>
                    </template>
                </v-list-item>

                <!-- <v-divider></v-divider> -->

                <v-list density="compact" nav>
                    <v-list-item
                        prepend-icon="mdi-home-city"
                        title="Home"
                        value="home"
                    ></v-list-item>
                    <v-list-item
                        prepend-icon="mdi-account"
                        title="My Account"
                        value="account"
                    ></v-list-item>
                    <v-list-item
                        prepend-icon="mdi-account-group-outline"
                        title="Users"
                        value="users"
                    ></v-list-item>
                </v-list>
            </v-navigation-drawer>
            <v-app-bar title="Application bar">
                <template v-slot:append>
                    <v-btn icon="mdi-heart"></v-btn>

                    <v-btn icon="mdi-magnify"></v-btn>

                    <v-btn icon="mdi-dots-vertical"></v-btn>

                    <div class="justify-content-center align-items-center">
                        <v-switch
                            v-model="model"
                            hide-details
                        ></v-switch>
                    </div>
                </template>
            </v-app-bar>
            <v-main
                style="min-height: 100vh"
            >
            Heello word
            </v-main>
        </v-layout>
    </v-card>
</template>
<script>
export default {
    data() {
        return {
            drawer: true,
            rail: true,
            showMessages: false,
            model: true,
        };
    },
    computed: {
        messages() {
            return this.showMessages ? ["Message"] : undefined;
        },
    },
};
</script>
