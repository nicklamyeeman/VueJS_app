<template web>
  <div class="w-page">
    <div class="w-container">    
      <img src="~/assets/logo.png" alt="logo" height="20%" width="20%">
      <HelloWorld :msg="msg"/>
      <myButton/>
      <myTextField/>
    </div>
  </div>
</template>
<template native>
  <Page>
    <ActionBar :title="navbarTitle"/>
    <GridLayout rows="auto, auto">
      <HelloWorld :msg="msg"/>
    </GridLayout>
    <myButton/>
    <myTextField/>
  </Page>
</template>
<script>

  import HelloWorld from '~/components/HelloWorld';
  import myButton from '~/components/myButton';
  import myTextField from '~/components/myTextField';

  const { VUE_APP_MODE, VUE_APP_PLATFORM } = process.env;

  export default {
    components: {
      myTextField,
      myButton,
      HelloWorld,
    },
    data() {
      return {
        navbarTitle: `App.vue`,
        msg: `Mode=${VUE_APP_MODE} and Platform=${VUE_APP_PLATFORM}`,
      };
    },
    methods: {
    }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style web>
  @import '~styles/style-one';

  .w-page {
    height: 100%;
    width: 100%;
  }
</style>
<style native>
  @import '~styles/style-one';
</style>
