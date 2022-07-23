<template>
  <div id="app">
    <div>comp 4</div>
    <HelloWorld4 />
    <hr />

    <div>comp 1</div>
    <HelloWorld />
    <hr />
    <div>comp 2</div>
    <HelloWorld2 />
    <hr />
    <div>comp 3</div>
    <HelloWorld3 v-bind:title="title" v-bind:num="num" />
    <input v-model="input" />
    <button @click="doAction">btn</button>
  </div>
</template>

<script>
import HelloWorld from './components/4syou/HelloWorld.vue';
import HelloWorld2 from './components/4syou/HelloWorld2.vue';
import HelloWorld3 from './components/4syou/HelloWorld3.vue';
import HelloWorld4 from './components/4syou/HelloWorld4.vue';

export default {
  name: 'app',
  components: {
    HelloWorld,
    HelloWorld2,
    HelloWorld3,
    HelloWorld4,
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
