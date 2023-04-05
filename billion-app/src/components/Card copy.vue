<template>
  <v-container>
    <v-card v-for="(item, i) in items" :key="i" cols="12" class="ma-4 pa-3">
      <v-row
        v-bind:style="[
          item.category === 'surveys'
            ? { background: '#24b4e0' }
            : { background: 'black' } && item.category === 'outcomes'
            ? { background: '#f24822' }
            : { background: 'black' } && item.category === 'output'
            ? { background: 'green' }
            : { background: 'black' },
        ]"
      >
        <!-- OuterBOx with white background -->
        <div class="outerBox">
          <div class="float-left innerBox px-5">
            <div class="d-flex justify-space-between">
              <h1 class="headline" v-text="item.title"></h1>
              <v-btn
                outlined
                small
                class="hidden-sm-and-down mt-2"
                v-bind:style="[
                  item.category === 'surveys'
                    ? { color: '#12c4be', background: '#d0f5f4' }
                    : { color: 'black' } && item.category === 'outcomes'
                    ? { color: '#f24822', background: '#ffac99' }
                    : { color: 'black' } && item.category === 'output'
                    ? { color: 'green', background: '#99f27e' }
                    : { color: 'black' },
                ]"
                >{{ item.category }}</v-btn
              >
            </div>
            <h6 class="hidden-sm-and-down" v-bind:style="{ color: '#90918e' }">
              {{ item.text }}
            </h6>
            <h5 v-bind:style="{ color: '#90918e' }">
              Project Name: {{ item.project }}
            </h5>
          </div>
          <div class="float-right">
            <div>
              <small v-bind:style="{ color: '#90918e' }">{{ item.date }}</small>
              <v-btn icon>
                <v-icon>mdi-dots-vertical</v-icon>
              </v-btn>
            </div>
            <v-btn
              outlined
              small
              class="hidden-md-and-up mt-6 mr-2"
              v-bind:style="[
                item.category === 'surveys'
                  ? { color: '#12c4be', background: '#d0f5f4' }
                  : { color: 'black' } && item.category === 'outcomes'
                  ? { color: '#f24822', background: '#ffac99' }
                  : { color: 'black' } && item.category === 'output'
                  ? { color: 'green', background: '#99f27e' }
                  : { color: 'black' },
              ]"
              >{{ item.category }}</v-btn
            >
          </div>
        </div>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "Card",
  data: () => ({
    items: [
      {
        title: "Pannier",
        text:
          "accumsan odio curabitur convallis duis consequat dui nec nisi volutpat eleifend donec",
        date: "21/01/2021",
        category: "surveys",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Stronghold",
        text:
          "tellus semper interdum mauris ullamcorper purus sit amet nulla quisque arcu libero rutrum",
        date: "21/01/2021",
        category: "outcomes",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Voyatouch",
        text:
          "consectetuer adipiscing elit proin risus praesent lectus vestibulum quam sapien varius ut blandit non interdum",
        date: "22/01/2021",
        category: "output",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Transcof",
        text: "congue eget semper rutrum nulla nunc purus phasellus in felis",
        date: "22/01/2021",
        category: "output",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Keylex",
        text:
          "sit amet consectetuer adipiscing elit proin risus praesent lectus vestibulum",
        date: "23/01/2021",
        category: "output",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Viva",
        text:
          "vestibulum quam sapien varius ut blandit non interdum in ante vestibulum ante ipsum",
        date: "23/01/2021",
        category: "output",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Vagram",
        text:
          "magna ac consequat metus sapien ut nunc vestibulum ante ipsum primis",
        date: "23/01/2021",
        category: "outcomes",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Keylex",
        text:
          "praesent blandit lacinia erat vestibulum sed magna at nunc commodo placerat praesent blandit nam",
        date: "23/01/2021",
        category: "surveys",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Daltfresh",
        text:
          "massa id lobortis convallis tortor risus dapibus augue vel accumsan",
        date: "24/01/2021",
        category: "surveys",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Voyatouch",
        text:
          "sem fusce consequat nulla nisl nunc nisl duis bibendum felis sed interdum",
        date: "24/01/2021",
        category: "output",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
    ],
  }),
};
</script>

<style scoped>
.outerBox {
  width: 100%;
  background-color: white;
  margin-left: 1%;
  padding: 5px;
}

.innerBox {
  width: 70%;
}
.innerBox * {
  padding: 5px 0px;
}
</style>