<template>
  <v-toolbar flat class="borderBottom">
    <v-toolbar-title>
      <v-row>
        <v-col class="ml-7">
          <v-img
            max-height="30"
            width="80%"
            src="..\assets\Iamwork.png"
          ></v-img>
        </v-col>
      </v-row>
    </v-toolbar-title>

    <v-spacer></v-spacer>

    <v-btn icon>
      <v-img max-height="35" max-width="35" src="..\assets\leaf.png"></v-img>
    </v-btn>
    <div id="region" class="hidden-sm-and-down text--secondary">
      <div>IN-Southern Region</div>
      <div>
        <div>
          <v-icon size="10"> mdi-lock </v-icon>
        </div>
        <div>Private</div>
      </div>
    </div>

    <router-link class="text-decoration-none" to="/">
      <v-btn icon>
        <v-icon>mdi-home</v-icon>
      </v-btn>
    </router-link>

    <v-btn icon>
      <v-icon>mdi-bell</v-icon>
    </v-btn>

    <v-btn class="hidden-sm-and-down" icon>
      <v-icon>mdi-help-circle</v-icon>
    </v-btn>

    <v-btn class="mr-2" icon>
      <v-avatar>
        <v-img
          max-height="40"
          max-width="40"
          src="https://lh3.googleusercontent.com/ogw/ADGmqu-aim41bmHeqAvGwcQvhtymYrivCOV9334yXK989g=s32-c-mo"
        ></v-img>
      </v-avatar>
    </v-btn>
  </v-toolbar>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped>
.borderBottom {
  border-bottom: 1px solid rgb(201, 198, 198);
}
#region {
  font-size: 12px;
  margin-left: 10px;
}

#region :nth-child(2) {
  display: flex;
  font-size: 10px;
}
</style>