<template>
  <v-card>
    <div>
      <v-toolbar flat dense>
        <v-toolbar-title>
          <v-icon
            class="rounded-circle"
            v-bind:style="{
              height: '30px',
              width: '30px',
              border: '1px solid grey',
            }"
            >mdi-format-list-bulleted</v-icon
          >
          My Task</v-toolbar-title
        >
        <v-spacer></v-spacer>

        <!-- SearchBox -->
        <div class="searchBox">
          <v-btn icon class="searchIcon">
            <v-icon>mdi-magnify</v-icon>
          </v-btn>
          <input class="input" />
        </div>

        <v-btn outlined small class="mx-1 pa-0 ma-0">
          <v-icon color="grey">mdi-filter-outline</v-icon>
          <small class="hidden-sm-and-down">filter</small>
        </v-btn>

        <v-btn outlined small class="mx-1 pa-0 ma-0">
          <v-icon color="grey">mdi-ammunition</v-icon>
        </v-btn>
      </v-toolbar>
    </div>

    <div>
      <v-tabs centered color="#b0b0b0">
        <v-tab
          v-bind:style="{ background: '#F5F5F5' }"
          active-class="transparent text--accent-4 "
        >
          Overdue
        </v-tab>
        <v-tab
          v-bind:style="{ background: '#F5F5F5' }"
          active-class="transparent text--accent-4"
        >
          Current
        </v-tab>
        <v-tab
          v-bind:style="{ background: '#F5F5F5' }"
          active-class="transparent text--accent-4"
        >
          Completed
        </v-tab>
      </v-tabs>
    </div>

    <!-- All cards display block -->
    <div class="feed mx-auto card">
      <Card />
    </div>
  </v-card>
</template>

<script>
import Card from "./Card";
export default {
  name: "Task",
  data: () => {
    return {
      active: false,
    };
  },
  components: {
    Card,
  },
  methods: {
    handleClick: function () {
      this.active = !this.active;
    },
  },
};
</script>

<style scoped>
.searchBox {
  border: 1px solid black;
  height: 26px;
  position: relative;
}

.input {
  position: relative;
  top: -10px;
  left: -10px;
  outline: none;
  border: none;
  height: "30px";
  width: 79%;
}

.searchIcon {
  position: relative;
  top: -12px;
  left: -10px;
  font-size: 50px;
}

.feed {
  height: 550px;
  overflow-y: scroll;
}

.feed::-webkit-scrollbar {
  display: none;
}

.card {
  width: 50%;
}

@media only screen and (max-width: 960px) {
  .status * {
    width: 30%;
  }

  .card {
    width: 100%;
  }
  .fixed {
    margin: 0 10%;
  }
  .searchBox {
    border: none;
  }
  .input {
    display: none;
  }
}
</style>