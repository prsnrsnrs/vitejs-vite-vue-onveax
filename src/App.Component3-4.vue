<template>
  <div id="app">
    <p>component4 start --------------</p>
    <HelloWorld4 />
    <p>component4 end --------------</p>
    <hr />
    <p>component3 start --------------</p>
    <HelloWorld3 v-bind:title="title" v-on:result-event="appAction" />
    <p>component3 end --------------</p>
    <hr />
    <button class="btn btn-primary" v-on:click="doAction">change title</button>

    <p>ev result: {{ result }}</p>
  </div>
</template>

<script>
import HelloWorld3 from './components/HelloWorld3.vue';
import HelloWorld4 from './components/HelloWorld4.vue';

export default {
  name: 'App',
  components: {
    HelloWorld3,
    HelloWorld4,
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
