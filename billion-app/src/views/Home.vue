<template>
  <v-container v-bind:style="{ background: 'whitesmoke' }">
    <div class="text-center">
      <h4>Savings Acccount Form</h4>
    </div>

    <v-icon>mdi-view-list-outline </v-icon>
    <span>Savings Acccount Form</span>
    <v-card>
      <v-card-text v-bind:style="{ overflowY: 'scroll', height: '500px' }">
        <v-layout row wrap>
          <v-flex xs12 md4>
            <b>Name Prefix</b>
            <p>Mr.</p>
          </v-flex>
          <v-flex xs12 md4
            ><b>First Name</b>
            <p>{{ team[0].name }}</p></v-flex
          >
          <v-flex xs12 md4
            ><b>Last Name</b>
            <p>Kapoor</p></v-flex
          >
        </v-layout>

        <v-layout row wrap>
          <v-flex xs12 md4>
            <b>Mobile Number</b>
            <p>91-786473821</p>
          </v-flex>
          <v-flex xs12 md4
            ><b>Date of Birth</b>
            <p>12-09-1990</p></v-flex
          >
          <v-flex xs12 md4
            ><b>Gender</b>
            <p>Male</p></v-flex
          >
        </v-layout>

        <v-layout row wrap>
          <v-flex xs12>
            <b>Adress Line 1</b>
            <p>F/100 infocity Ave</p>
          </v-flex>
          <v-flex xs12
            ><b>Adress Line 2</b>
            <p>Near info height Patna</p></v-flex
          >
        </v-layout>
        <v-layout row wrap>
          <v-flex xs12 md4>
            <b>City</b>
            <p>Bhopal</p>
          </v-flex>
          <v-flex xs12 md4
            ><b>State</b>
            <p>Madhya Pradesh</p></v-flex
          >
          <v-flex xs12 md4
            ><b>Post Code</b>
            <p>758432</p></v-flex
          >
        </v-layout>

        <v-layout row wrap>
          <v-switch
            label="Is Permanent address same as Communication address? "
            color="pink"
            value="true"
          ></v-switch>
        </v-layout>

        <v-layout row wrap>
          <v-flex xs12 md4>
            <b>Email</b>
            <p>Demo@gmail.com</p>
          </v-flex>
          <v-flex xs12 md4
            ><b>Religon</b>
            <p>Hindu</p></v-flex
          >
          <v-flex xs12 md4
            ><b>Category</b>
            <p>Gernal</p></v-flex
          >
        </v-layout>

        <v-layout row wrap>
          <v-flex xs12 md4>
            <b>Mother's Name</b>
            <p>Sujata kapoor</p>
          </v-flex>
          <v-flex xs12 md4
            ><b>Father's Name</b>
            <p>Raj kapooer</p></v-flex
          >
        </v-layout>

        <v-layout row wrap>
          <v-flex xs12 md4><h3>Are you Married?</h3></v-flex>
          <v-flex xs12 md4
            ><v-switch
              v-bind:style="{ marginTop: '0' }"
              dense
              disabled
              v-model="switch1"
              color="pink"
            ></v-switch
          ></v-flex>
        </v-layout>

        <v-layout row wrap>
          <v-flex xs12 md4>
            <b>Education</b>
            <p>Post Graduate</p>
          </v-flex>
          <v-flex xs12 md4
            ><b>Occupation</b>
            <p>Doctor</p></v-flex
          >
          <v-flex xs12 md4
            ><b>Annual income</b>
            <p>1,00,000</p></v-flex
          >
        </v-layout>

        <v-layout row wrap>
          <v-flex xs12 md4><h3>Nominee Required</h3></v-flex>
          <v-flex xs12 md4
            ><v-switch
              v-bind:style="{ marginTop: '0' }"
              dense
              disabled
              v-model="switch1"
              color="pink"
            ></v-switch
          ></v-flex>
        </v-layout>

        <v-layout row wrap>
          <v-flex xs12>
            <b>Upload Photo of the customer</b>
            <v-img :src="__dirname + 'b6F1hk_6_400x400_26_0.jpg'"></v-img>
          </v-flex>
          <v-flex xs12
            ><b>Signature</b>
            <v-img></v-img>
          </v-flex>
        </v-layout>

        <v-layout column wrap>
          <v-layout row wrap>
            <v-flex xs12 md4><h3>Would you like Cheque book</h3></v-flex>
            <v-flex justify-end
              ><v-switch
                v-bind:style="{ marginTop: '0' }"
                dense
                disabled
                v-model="switch1"
                color="pink"
              ></v-switch></v-flex
          ></v-layout>

          <v-layout row wrap>
            <v-flex xs12 md4><h3>Would you like Debit card</h3></v-flex>
            <v-flex
              ><v-switch
                v-bind:style="{ marginTop: '0' }"
                dense
                disabled
                v-model="switch1"
                color="pink"
              ></v-switch></v-flex
          ></v-layout>

          <v-layout row wrap>
            <v-flex xs12 md4><h3>Mobile Banking</h3></v-flex>
            <v-flex
              ><v-switch
                v-bind:style="{ marginTop: '0' }"
                dense
                disabled
                v-model="switch1"
                color="pink"
              ></v-switch></v-flex
          ></v-layout>

          <v-layout row wrap>
            <v-flex xs12 md4><h3>Internet Banking</h3></v-flex>
            <v-flex
              ><v-switch
                v-bind:style="{ marginTop: '0' }"
                dense
                disabled
                v-model="switch2"
                color="pink"
              ></v-switch></v-flex
          ></v-layout>

          <v-layout class="d-flex" row wrap>
            <div class="mt-1"><h3>SMS Alerts</h3></div>
            <div>
              <v-switch
                v-bind:style="{ marginTop: '0' }"
                dense
                disabled
                v-model="switch1"
                color="pink"
              ></v-switch></div
          ></v-layout>

          <v-layout row wrap>
            <v-flex xs12 md4><h3>Email ALerts</h3></v-flex>
            <v-flex
              ><v-switch
                v-bind:style="{ marginTop: '0' }"
                dense
                disabled
                v-model="switch2"
                color="pink"
              ></v-switch
            ></v-flex>
          </v-layout>

          <v-layout row wrap>
            <v-flex
              ><h3>
                Do you want to activate DND feature on your account
              </h3></v-flex
            >
            <v-flex
              ><v-switch
                v-bind:style="{ marginTop: '0' }"
                dense
                disabled
                v-model="switch2"
                color="pink"
              ></v-switch
            ></v-flex>
          </v-layout>
        </v-layout>
      </v-card-text>
      <v-card-actions>
        <v-btn
          dark
          depressed
          class="pl-13 pr-13"
          color="#A50E39"
          @click="Submit"
        >
          Submit
        </v-btn>
        <v-btn class="pl-15 pr-15" outlined color="grey" @click="edit()">
          Edit
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "Home",
  components: {},
  data() {
    return {
      switch1: true,
      switch2: false,
      team: [
        {
          name: "Rashmi singh",
          role: "admin",
          taskCounts: 1,
          progress: 34,
        },
        {
          name: "hritika singh",
          role: "admin",
          taskCounts: 1,
          progress: 92,
        },
        {
          name: "xyz singh",
          role: "admin",
          taskCounts: 1,
          progress: 92,
        },
        {
          name: "sanju kumar",
          role: "admin",
          taskCounts: 1,
          progress: 56,
        },
        {
          name: "Rashmi singh",
          role: "admin",
          taskCounts: 9,
          progress: 100,
        },
        {
          name: "jeetal singh",
          role: "admin",
          taskCounts: 1,
          progress: 87,
        },
        {
          name: "Rashmi singh",
          role: "admin",
          taskCounts: 4,
          progress: 23,
        },
        {
          name: "Rashmi singh",
          role: "admin",
          taskCounts: 1,
          progress: 34,
        },
      ],
    };
  },
};
</script>


<style scoped>
::-webkit-scrollbar {
  display: none;
}
</style>



