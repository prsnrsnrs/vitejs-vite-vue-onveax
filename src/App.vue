<template>
  <div id="app">
    <p>comp start</p>
    <HelloWorld3 v-bind:title="title" v-on:result-event="appAction" />
    <p>comp end</p>
    <hr />
    <button class="btn btn-primary" v-on:click="doAction">change title</button>

    <p>ev result: {{ result }}</p>
  </div>
</template>

<script>
import HelloWorld3 from './components/HelloWorld3.vue';

export default {
  name: 'App',
  components: {
    HelloWorld3,
  },
  data() {
    return {
      // message: 'HELLO',
      title: 'HELLO',
      result: 'no event yet',
    };
  },
  methods: {
    doAction() {
      var input = prompt('new title:');
      // this.message = input;
      this.title = input;
    },
    appAction(message) {
      this.result = '(*** you send:"' + message + '". ***)';
    },
  },
};
</script>
