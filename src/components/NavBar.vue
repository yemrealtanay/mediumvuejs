<template>
<nav>
<v-app-bar flat app>
  <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
  <v-app-bar-title class="text-uppercase grey--text">
    <span class="font-weight-black display-1">Medium</span>
    <span class="font-weight-light">Vue Projesi</span>
  </v-app-bar-title>
  <v-spacer></v-spacer>
  <v-btn class="primary ma-2">
    <span>SıgnIn</span>
    <v-icon right>mdi-login</v-icon>
  </v-btn>
  <v-btn class="success ma-2">
    <span>LogIn</span>
    <v-icon right>mdi-key</v-icon>
  </v-btn>
  <v-btn class="flat pink accent-3 white--text ma-2">
    <span>LogOut</span>
    <v-icon right>mdi-logout</v-icon>
  </v-btn>
</v-app-bar>

<v-navigation-drawer absolute bottom app v-model="drawer">
  <v-list rounded dans nav>
    <v-subheader>MENU</v-subheader>
    <v-list-item-group v-model="selectedItem" color="primary">
      <v-list-item
          v-for="(item, i) in items"
          :key="i"
          link
          :to="item.route"
      >
        <v-list-item-icon>
          <v-icon v-text="item.icon"></v-icon>
        </v-list-item-icon>
        <v-list-item-content>
          <v-list-item-title v-text="item.text"></v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list-item-group>
  </v-list>
</v-navigation-drawer>
</nav>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      items: [
        { icon: "mdi-view-dashboard", text: "Dashboard", route: "/" },
        {
          icon: "mdi-arrow-up-bold-box-outline",
          text: "About",
          route: "/about",
        },
      ],
    };
  },
};
</script>