<template>
  <GridLayout rows="auto, auto">
    <Label class="message" :text="msg" row="0" horizontalAlignment="center"/>
    <Image src="~/components/icon.png" row="1" class="m-40"/>
  </GridLayout>
</template>
<script>
  export default {
    name: 'HelloWorld',
    props: {
      msg: String
    }
  };
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .message {
    color: #420000;
  }

  Image {
    height: 20%;
    width: 20%;
    margin-top: 20px;
  }
</style>
