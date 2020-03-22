<template>
  <TextField :text="tempMessage" hint="Enter Text Here"
    returnPress="submit"/>
</template>
<script>
  export default {
    name: 'myTextField',
    data() {
        return {
            tempMessage: ""
        };
    },
    methods: {
        submit: function() {
            this.$emit("inputData", this.tempMessage);
            this.tempMessage = "";
        }
    }
  };
</script>