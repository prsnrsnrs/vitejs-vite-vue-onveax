<template>
  <div id="app">
    <HelloWorld />
    <hr />
    <HelloWorld2 />
  </div>
</template>

<script>
import HelloWorld from './components/4syou/HelloWorld.vue';
import HelloWorld2 from './components/4syou/HelloWorld2.vue';

export default {
  name: 'app',
  components: {
    HelloWorld,
    HelloWorld2,
  },
};
</script>
