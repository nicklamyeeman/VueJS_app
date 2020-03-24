<template>
  <div>
      <input
        placeholder="Enter Text Here"
        v-model="tempMessage"
        @keyup.enter="submit"
      />
  </div>
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
            console.log(this.tempMessage);
            this.$emit("inputData", this.tempMessage);
            this.tempMessage = "";
        }
    }
  };
</script>