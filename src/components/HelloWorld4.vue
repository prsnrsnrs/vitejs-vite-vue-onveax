<template>
  <div>
    <div>title: {{ title }}</div>
    <div ref="msg">message: {{ message }}</div>
    <div><button v-on:click="doAction">btn</button></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: 'hello',
      message: 'first message',
    };
  },
  mounted() {
    this.counter = 0; // data()で連携してない
  },
  methods: {
    doAction() {
      this.counter++;
      console.log(this.counter);
      // 3-23あたりの、$ref サンプル
      this.$refs.msg.innerHTML += '<h6>' + this.counter + '</h6>';
    },
  },
};
</script>
