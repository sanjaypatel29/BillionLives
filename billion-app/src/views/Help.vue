<template>
  <div class="text-center">
    <input type="text" v-model="price" />{{ price }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      price: null,
    };
  },
  // method:{
  //    CommaFeature (newValue) {
  //     var x = newValue.replace(/\D/g, "");
  //     x = x.toString();
  //     var lastThree = x.substring(x.length - 3);
  //     var otherNumbers = x.substring(0, x.length - 3);
  //     if (otherNumbers != "") lastThree = "," + lastThree;
  //     var res = otherNumbers.replace(/\B(?=(\d{2})+(?!\d))/g, ",") + lastThree;
  //     return res
  //   }
  // },
  //  filter: {
  //   commasCurrency (newValue) {
  //     // var x = newValue.replace(/\D/g, "");
  //     // x = x.toString();
  //     // var lastThree = x.substring(x.length - 3);
  //     // var otherNumbers = x.substring(0, x.length - 3);
  //     // if (otherNumbers != "") lastThree = "," + lastThree;
  //     // var res = otherNumbers.replace(/\B(?=(\d{2})+(?!\d))/g, ",") + lastThree;
  //     // this.$nextTick(() => (this.price = res));
  //     return `$newValue.toLocaleString('en-IN')`;
  //   }
  // }

  watch: {
    price: function (newValue) {
      var x = newValue.replace(/\D/g, "");
      x = x.toString();
      var lastThree = x.substring(x.length - 3);
      var otherNumbers = x.substring(0, x.length - 3);
      if (otherNumbers != "") lastThree = "," + lastThree;
      var res = otherNumbers.replace(/\B(?=(\d{2})+(?!\d))/g, ",") + lastThree;
      this.$nextTick(() => (this.price = res));
    },
  },
};
</script>