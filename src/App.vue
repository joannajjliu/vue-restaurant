<template>
    <v-app>
        <font-awesome-icon :icon="['fab', 'twitter']" class="icon alt"/>
        <font-awesome-icon :icon="['far', 'user']"></font-awesome-icon>
        <app-navigation></app-navigation>
        <v-content transition="slide-x-transition">
            <router-view></router-view>
        </v-content>
    </v-app>
</template>

<script>
import AppNavigation from './components/AppNavigation';
export default {
    name: 'App',
    components: {
        AppNavigation
    }
};
</script>

<style>
</style>