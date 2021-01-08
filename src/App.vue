<template>
  <v-app>

    <TopToolbar></TopToolbar>


    <v-content>
      <router-view></router-view>
    </v-content>
    
    <BottomNav></BottomNav>

  </v-app>
</template>

<script>
  import TopToolbar from './components/TopToolbar.vue';
  import BottomNav from './components/BottomNav.vue';

    export default {
        components: {
          TopToolbar,
          BottomNav
        },
        data() {
            return {
                activeItem: 'top'
            }
        },
        methods: {
            toggleMenu() {
                this.showMenu = !this.showMenu;
            },
            doNothing() {}

        },
    }
</script>