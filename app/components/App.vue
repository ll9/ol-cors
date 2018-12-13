<template>
    <Page>
        <ActionBar title="Welcome to NativeScript-Vue!"/>
        <GridLayout columns="*" rows="*">
            <Button class="message" :text="msg" @tap="nav" col="0" row="0"/>
        </GridLayout>
    </Page>
</template>

<script>

import SecondPage from './SecondPage';

  export default {
    data() {
      return {
        msg: 'Hello World!'
      }
    },
    methods: {
        nav() {
            this.$navigateTo(SecondPage);
        }
    }
  }
</script>

<style scoped>
    ActionBar {
        background-color: #53ba82;
        color: #ffffff;
    }

    .message {
        vertical-align: center;
        text-align: center;
        font-size: 20;
        color: #333333;
    }
</style>
