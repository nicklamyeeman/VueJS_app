<template>
  <div>
      <button v-on:click="onButtonClick()">KESKIDI?</button>
  </div>
</template>
<script>
  export default {
    name: 'myButton',
    props: {
      msg: String,
    },
    methods: {
      onButtonClick() {
        console.log(this.msg);
      },
    }, 
    watch: {
      msg() {
        console.log(this.msg);
      }
    }
  };
</script>