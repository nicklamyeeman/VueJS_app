<template>
    <Button text="My button" class="my-button" @tap="onButtonTap"></Button>
</template>
<script>
  export default {
    name: 'myButton',

    methods: {
      onButtonTap() {
        console.log("You tapped the button!");
      },
    }
};

</script>
<style>
  .my-button {
      width: 200px;
      height: 200px;
      background-color: lightseagreen;
      border-color: darkolivegreen;
      border-radius: 20;
      border-width: 1;
      color: whitesmoke;
      font-size: 18;
  }

  .my-button:active {
      background-color: whitesmoke;
      border-color: darkolivegreen;
      border-radius: 20;
      border-width: 1;
      color: lightseagreen;
      font-size: 18;
  }
</style>