<template>
  <v-app>
    <v-app-bar
      app
      dark
      dense
    >
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
        <v-toolbar-title>Hours</v-toolbar-title>
        <v-btn text to="about">About</v-btn>
        <v-btn text to="/">Hello</v-btn>
        <v-spacer></v-spacer>
        <v-btn icon @click.stop="setupdrawer = !setupdrawer">
            <v-icon>mdi-cog</v-icon>
        </v-btn>
        <v-navigation-drawer v-model="setupdrawer" right app>
            <v-list dense>
                <v-list-item to="login">
                    <v-list-item-action>
                        <v-icon>mdi-lock</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                        <v-list-item-title>Login</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </v-app-bar>
    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
//import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
//    HelloWorld,
  },

  data: () => ({
    setupdrawer:false
  }),
};
</script>
