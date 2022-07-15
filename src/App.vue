<template>
  <div id="app">
    <HelloWorld3 v-bind:title="message" />
    <hr />
    <button class="btn btn-primary" v-on:click="doAction">change title</button>
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
      message: 'HELLO',
    };
  },
  methods: {
    doAction() {
      var input = prompt('new title:');
      this.message = input;
    },
  },
};
</script>
