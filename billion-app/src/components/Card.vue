<template>
  <v-container>
    <v-card v-for="(item, i) in items" :key="i" cols="12" class="mt-5">
      <v-row class="pa-0 ma-0">
        <v-col cols="11">
          <v-row>
            <h5 class="pa-3">adasdadassda adsa adasd</h5>
          </v-row>
          <v-row>
            <v-col>number</v-col>
            <v-col
              ><v-btn
                outlined
                small
                class=""
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
              ></v-col
            >
            <v-col>12/20/1990</v-col>
            <v-col>monthly</v-col>
            <v-col>To Data Collect</v-col>
            <v-col>Teachers</v-col>
            <v-col
              ><v-btn icon>
                <v-icon>mdi-dots-vertical</v-icon>
              </v-btn></v-col
            >
          </v-row>
        </v-col>
        <v-col cols="1" class="pa-0 ma-0">
          <div
            class="d-flex justify-center"
            style="
              background: blue;
              writing-mode: vertical-rl;
              color: white;
              height: 25%;
            "
          >
            <p class="textHover">abc</p>
          </div>
        </v-col>
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
        text: "accumsan odio curabitur convallis duis consequat dui nec nisi volutpat eleifend donec",
        date: "21/01/2021",
        category: "surveys",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Stronghold",
        text: "tellus semper interdum mauris ullamcorper purus sit amet nulla quisque arcu libero rutrum",
        date: "21/01/2021",
        category: "outcomes",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Voyatouch",
        text: "consectetuer adipiscing elit proin risus praesent lectus vestibulum quam sapien varius ut blandit non interdum",
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
        text: "sit amet consectetuer adipiscing elit proin risus praesent lectus vestibulum",
        date: "23/01/2021",
        category: "output",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Viva",
        text: "vestibulum quam sapien varius ut blandit non interdum in ante vestibulum ante ipsum",
        date: "23/01/2021",
        category: "output",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Vagram",
        text: "magna ac consequat metus sapien ut nunc vestibulum ante ipsum primis",
        date: "23/01/2021",
        category: "outcomes",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Keylex",
        text: "praesent blandit lacinia erat vestibulum sed magna at nunc commodo placerat praesent blandit nam",
        date: "23/01/2021",
        category: "surveys",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Daltfresh",
        text: "massa id lobortis convallis tortor risus dapibus augue vel accumsan",
        date: "24/01/2021",
        category: "surveys",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
      {
        title: "Voyatouch",
        text: "sem fusce consequat nulla nisl nunc nisl duis bibendum felis sed interdum",
        date: "24/01/2021",
        category: "output",
        project: "Mahila kisan Sashaktikaran Pariyojna(MKSP)",
      },
    ],
  }),
};
</script>

<style scoped>
.textHover {
  display: none;
}
.textHover:hover {
  transition: all 0.2s ease;
  display: block;
  height: 80px;
}
</style>