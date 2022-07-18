<template>
  <div id="app">
    <HelloWorld />
    <hr />
    <HelloWorld2 />
    <hr />
    <HelloWorld3 v-bind:title="title" v-bind:num="num" />
    <input v-model="input" />
    <button @click="doAction">btn</button>
  </div>
</template>

<script>
import HelloWorld from './components/4syou/HelloWorld.vue';
import HelloWorld2 from './components/4syou/HelloWorld2.vue';
import HelloWorld3 from './components/4syou/HelloWorld3.vue';

export default {
  name: 'app',
  components: {
    HelloWorld,
    HelloWorld2,
    HelloWorld3,
  },
  data() {
    return {
      title: 'title desuuu',
      num: 'abccc',
      input: 'input here',
    };
  },
  methods: {
    doAction() {
      this.num = this.input;
    },
  },
};
</script>
