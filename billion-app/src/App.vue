<template>
  <v-app>
    <!-- Top network bar visible only for mobile screen -->
    <div class="hidden-md-and-up">
      <v-system-bar window color="white">
        <span class="font-weight-bold ml-1" v-bind:style="{ color: 'black' }"
          >12:30</span
        >
        <v-spacer></v-spacer>
        <v-icon color="black">mdi-signal</v-icon>
        <v-icon color="black">mdi-wifi</v-icon>
        <v-icon color="black">mdi-battery</v-icon>
      </v-system-bar>
    </div>

    <!-- sidebar,navbar visible for all screen -->
    <div class="d-flex">
      <div class="sidebar"><Drawer /></div>
      <div v-bind:style="{ width: '100%' }">
        <div>
          <Navbar />
        </div>
        <div>
          <!-- Here Pages will be change according to routes -->
          <router-view />
        </div>
      </div>
    </div>
  </v-app>
</template>

<script>
import Drawer from "./components/Drawer";
import Navbar from "./components/Navbar";
export default {
  name: "App",
  components: {
    Navbar,
    Drawer,
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
.sidebar {
  width: auto;
  height: auto;
  z-index: 1;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

@media only screen and (max-width: 600px) {
  .sidebar {
    width: 0px;
    margin-top: 5px;
  }
}
</style>
