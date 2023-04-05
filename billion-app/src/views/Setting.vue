<template>
  <div>
    <money v-model="price" v-bind="money"></money> {{price}}
  </div>
</template>
 
<script>
  import {Money} from 'v-money'
 
  export default {
    components: {Money},
 
    data () {
      return {
        price: 0,
        money: {
          decimal: '.',
          thousands: ',',
          prefix: 'Rs ',
          suffix: '',
          precision: 0,
          masked: false
        }
      }
    }
  }
</script> 