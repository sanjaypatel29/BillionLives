<template>
  <div class="grey lighten-5 dashboard">
    <div class="pa-8 mr-15">
      <!-- Desktop Icon and Heading -->
      <div class="d-flex">
        <v-card
          class="rounded-circle mt-2"
          v-bind:style="{
            height: '34px',
            width: '34px',
            border: '1px solid grey',
          }"
        >
          <v-icon color="light-blue" class="pa-1 mt-1"
            >mdi-remote-desktop
          </v-icon>
        </v-card>
        <h1 class="ml-2">Dashboard</h1>
      </div>
      <!-- 3 Task Status Box -->
      <v-row class="mt-3 justify-space-between">
        <v-col class="white pa-4">
          <v-row>
            <v-col lg="8">
              <h2>Completed Task</h2>
              <h1>70%</h1>
              <small>Task Completed</small>
              <p class="mt-5">
                The Task Comppletion progress is increased to 70% out of 100%
              </p>
            </v-col>
            <v-col lg="4">
              <div class="circle"><h1 class="ma-7">70%</h1></div>
            </v-col>
          </v-row>
        </v-col>

        <v-col class="white pa-4 mr-12 ml-12">
          <v-row>
            <v-col lg="8">
              <h2>Active Task</h2>
              <h1>40%</h1>
              <small>Task Active</small>
              <p class="mt-5">
                The Active Task progress is decreased to 40% out of 100%
              </p>
            </v-col>
            <v-col lg="4">
              <div class="circle"><h1 class="ma-7">40%</h1></div>
            </v-col>
          </v-row>
        </v-col>

        <v-col class="white pa-4">
          <v-row>
            <v-col lg="8">
              <h2>Assigned Task</h2>
              <h1>70%</h1>
              <small>Task Assigned</small>
              <p class="mt-5">
                The Task Assigned progress is increased to 90% out of 100%
              </p>
            </v-col>
            <v-col lg="4">
              <div class="circle"><h1 class="ma-7">90%</h1></div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>

      <!-- Notification and task block -->
      <v-row class="mt-8">
        <v-card class="notificationCard pa-2">
          <h3 class="ml-3 mb-4">Notification</h3>
          <div class="cardFeed mt-2">
            <!-- Notification data -->
            <v-card class="d-flex mt-2">
              <div>
                <v-icon color="light-blue" class="pa-1 mt-5"
                  >mdi-remote-desktop
                </v-icon>
              </div>
              <div class="ml-2">
                <h4>Subscription</h4>
                <small
                  >Your subscription is about to expire within 3 days</small
                >
              </div>
              <div class="ml-9">
                <small>8:29</small>
              </div>
            </v-card>

            <v-card class="d-flex mt-2">
              <div>
                <v-icon color="light-blue" class="pa-1 mt-5"
                  >mdi-remote-desktop
                </v-icon>
              </div>
              <div class="ml-2">
                <h4>Subscription</h4>
                <small
                  >Your subscription is about to expire within 3 days</small
                >
              </div>
              <div class="ml-9">
                <small>8:29</small>
              </div>
            </v-card>

            <v-card class="d-flex mt-2">
              <div>
                <v-icon color="light-blue" class="pa-1 mt-5"
                  >mdi-remote-desktop
                </v-icon>
              </div>
              <div class="ml-2">
                <h4>Subscription</h4>
                <small
                  >Your subscription is about to expire within 3 days</small
                >
              </div>
              <div class="ml-9">
                <small>8:29</small>
              </div>
            </v-card>

            <v-card class="d-flex mt-2">
              <div>
                <v-icon color="light-blue" class="pa-1 mt-5"
                  >mdi-remote-desktop
                </v-icon>
              </div>
              <div class="ml-2">
                <h4>Subscription</h4>
                <small
                  >Your subscription is about to expire within 3 days</small
                >
              </div>
              <div class="ml-9">
                <small>8:29</small>
              </div>
            </v-card>

            <v-card class="d-flex mt-2">
              <div>
                <v-icon color="light-blue" class="pa-1 mt-5"
                  >mdi-remote-desktop
                </v-icon>
              </div>
              <div class="ml-2">
                <h4>Subscription</h4>
                <small
                  >Your subscription is about to expire within 3 days</small
                >
              </div>
              <div class="ml-9">
                <small>8:29</small>
              </div>
            </v-card>

            <v-card class="d-flex mt-2">
              <div>
                <v-icon color="light-blue" class="pa-1 mt-5"
                  >mdi-remote-desktop
                </v-icon>
              </div>
              <div class="ml-2">
                <h4>Subscription</h4>
                <small
                  >Your subscription is about to expire within 3 days</small
                >
              </div>
              <div class="ml-9">
                <small>8:29</small>
              </div>
            </v-card>

            <v-card class="d-flex mt-2">
              <div>
                <v-icon color="light-blue" class="pa-1 mt-5"
                  >mdi-remote-desktop
                </v-icon>
              </div>
              <div class="ml-2">
                <h4>Subscription</h4>
                <small
                  >Your subscription is about to expire within 3 days</small
                >
              </div>
              <div class="ml-9">
                <small>8:29</small>
              </div>
            </v-card>

            <v-card class="d-flex mt-2">
              <div>
                <v-icon color="light-blue" class="pa-1 mt-5"
                  >mdi-remote-desktop
                </v-icon>
              </div>
              <div class="ml-2">
                <h4>Subscription</h4>
                <small
                  >Your subscription is about to expire within 3 days</small
                >
              </div>
              <div class="ml-9">
                <small>8:29</small>
              </div>
            </v-card>
          </div>
        </v-card>

        <v-card class="myTaskCard pa-2">
          <h3 class="ml-3 mb-4">My task</h3>
          <div class="cardFeed mt-2">
            <Card />
          </div>
        </v-card>
      </v-row>
    </div>
  </div>
</template>


<script>
import Card from "./Card";
export default {
  name: "Dashboard",
  components: {
    Card,
  },
};
</script>


<style scoped>
.dashboard {
  height: 660px;
}

.circle {
  width: 130px;
  height: 130px;
  border: 10px solid blue;
  border-radius: 50%;
  margin-top: 12px;
  margin-right: 10px;
}
.notificationCard {
  width: 31%;
}

.myTaskCard {
  width: 65%;
  margin-left: 4%;
}
.cardFeed {
  height: 330px;
  overflow-y: scroll;
}

.cardFeed::-webkit-scrollbar {
  display: none;
}
</style>