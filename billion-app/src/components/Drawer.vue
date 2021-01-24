<template>
  <div>
    <!-- For large screen -->
    <v-navigation-drawer
      permanent
      class="hidden-sm-and-down item"
      expand-on-hover
    >
      <v-app-bar-nav-icon class="mb-12 mt-3 ml-2"></v-app-bar-nav-icon>

      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-remote-desktop </v-icon>
            </v-list-item-icon>
            <v-list-item-title>Monitor</v-list-item-title>
          </v-list-item>

          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-file-cog</v-icon>
            </v-list-item-icon>
            <v-list-item-title>File</v-list-item-title>
          </v-list-item>

          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-cog-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Settings</v-list-item-title>
          </v-list-item>
          <div v-bind:style="{ height: '400px' }"></div>

          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-help-circle</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Help</v-list-item-title>
          </v-list-item>
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-message-processing</v-icon>
            </v-list-item-icon>
            <v-list-item-title>message</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <!-- for small screen -->
    <v-app-bar-nav-icon
      @click.stop="drawer = !drawer"
      class="hidden-md-and-up item"
    ></v-app-bar-nav-icon>
    <v-navigation-drawer v-model="drawer" absolute left temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-remote-desktop </v-icon>
            </v-list-item-icon>
            <v-list-item-title>Monitor</v-list-item-title>
          </v-list-item>

          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-file-cog</v-icon>
            </v-list-item-icon>
            <v-list-item-title>File</v-list-item-title>
          </v-list-item>

          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-cog-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Settings</v-list-item-title>
          </v-list-item>
          <div v-bind:style="{ height: '400px' }"></div>

          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-help-circle</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Help</v-list-item-title>
          </v-list-item>
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-message-processing</v-icon>
            </v-list-item-icon>
            <v-list-item-title>message</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: "Drawer",
  data: () => ({
    drawer: false,
    group: null,
  }),

  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>

<style scoped>
</style>

