<template>

  <v-bottom-navigation
    app
    fixed
    grow
    v-model="activeItem"
    color="primary"
  >
    <v-btn value="top" :to="{ path: '/'}">
      <span>Top Stories</span>
      <v-icon>thumb_up</v-icon>
    </v-btn>

    <v-btn value="code" :to="{ name: 'code-examples'}">
      <span>Code Examples</span>
      <v-icon>code</v-icon>
    </v-btn>

    <v-btn value="favorites" :to="{ name: 'my-favorites'}">
      <span>Favorites</span>
      <v-icon>favorite</v-icon>
    </v-btn>
  </v-bottom-navigation>

</template>

<script>
    export default {
        name: 'BottomNav',
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