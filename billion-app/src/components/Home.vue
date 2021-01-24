<template>
  <v-container fluid v-bind:style="{ margin: '0px', padding: '0px' }">
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

    <!-- sidebar,navbar and card visible for all screen -->
    <div class="d-flex">
      <div class="sidebar"><Drawer /></div>
      <div v-bind:style="{ width: '100%' }">
        <div>
          <Navbar />
        </div>
        <div class="ma-3">
          <Task />
        </div>
      </div>
    </div>
  </v-container>
</template>


<script>
import Drawer from "./Drawer";
import Navbar from "./Navbar";
import Task from "./Task";
export default {
  name: "HOME",
  components: {
    Navbar,
    Drawer,
    Task,
  },
};
</script>


<style scoped>
.sidebar {
  width: auto;
  height: auto;
  z-index: 1;
}

@media only screen and (max-width: 600px) {
  .sidebar {
    width: 0px;
    margin-top: 5px;
  }
}
</style>